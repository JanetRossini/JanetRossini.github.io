---
date: "2024-04-13-0704"
title: Blender Button with Parameters
---

Our Blender Python script has several buttons that do almost the same thing. So we had several button classes, differing only a small amount. It took days to find the info here, but here's how we created a button that takes parameters.

We build vehicles and rides in Second Life. Lately we're using Blender to design them, and importing what we need into SL. Our Python code has a number of buttons that are essentially the same, except that they access a different file. An operator button points to a class, and since these classes were sightly different, we had a number of classes that looked like this:

~~~python
class RCG_OT_addtrack05(Operator):
    """ Add an object called Track05 from a specific file """
    bl_idname = "rcg.addtrackobject05"
    bl_label = "0.5m"
    bl_options = {"REGISTER", "UNDO"}

    @classmethod
    def poll(cls, context):
        return context.mode == "OBJECT"

    def execute(self, context):
        name = "track05"
        filepath, directory, filename = make_elements(name)
        bpy.ops.wm.append(filepath=filepath,
                          directory=directory,
                          filename=filename)
        track05 = bpy.data.objects[name]
        track05.select_set(state=True, view_layer=bpy.context.view_layer)
        bpy.context.view_layer.objects.active = track05
        return {'FINISHED'}
~~~

Each of these classes had its own button, like this one:

~~~python
    def draw(self, context):
        ...
        row = col.row()
        row.operator("rcg.addtrackobject05")
        row.operator("rcg.addtrackobject10")
        ...
~~~

We want all the buttons, but wqe do not want all the duplicated classes. We need a button that can provide a parameter, and a class that accepts one.

It turns out that Blender's button classes cannot accept new parameters using the conventional `__init__` method you'd typically use in Python to give a class instance its starting values. But somehow we need to do three things:

1. We must declare a parameter in the class;
2. We must use that parameter to give the class different behavior;
3. We must set the parameter differently for each button.

The second part is easy. If we had an attribute in our class named rcg_file, which contained the right string, we could use it like this:

~~~python
    def execute(self, context):
        if self.rcg_file != "":
            name = self.rcg_file
        else:
            name = "track05"
            self.report({"WARNING"}, "defaulting to " + name)
        self.report({"INFO"}, "adding " + name)
        filepath, directory, filename = make_elements(name)
        bpy.ops.wm.append(filepath=filepath,
                          directory=directory,
                          filename=filename)
        track05 = bpy.data.objects[name]
        track05.select_set(state=True, view_layer=bpy.context.view_layer)
        bpy.context.view_layer.objects.active = track05
        return {'FINISHED'}
~~~

We check it for blank mostly for historical reasons: I wasn't sure at first whether the parameter would get there, so I check it for empty and set it to a known-good value. We could just use the value if we were more confident.

But how can we declare `rcg_file`? The secret sauce in our case is StringProperty, and some very obscure Python syntax:

~~~python
class RCG_OT_importObject(Operator):
    """ Add an object from a premade blender file """
    bl_idname = "rcg.importobject"
    bl_label = "Size"
    bl_options = {"REGISTER", "UNDO"}

    rcg_file: bpy.props.StringProperty(name="Default Name")
~~~

The syntax is a "type annotation" or "type hint", and how Blender uses it is a deep mystery. What we need to know is that this ine does what we need so that at run time, our button can reference `rcg_file` as a class variable, and that it can contain a value set at run time, which we'll do in a moment. If we do not set it, by the way, it will be an empty string.

There are also IntProperty, BoolProperty, and FloatProperty. You can [read the Blender docs](https://docs.blender.org/api/current/bpy.props.html) here for more detail. The trick is finding that page when you need it.

Finally, we need to set the correct value as part of defining our buttons. It goes like this:

~~~python
    # noinspection SpellCheckingInspection
    def draw(self, context):
        ...
        row = col.row()
        op05 = row.operator("rcg.importobject", text="0.5m")
        op05.rcg_file = "track05"
        op05 = row.operator("rcg.importobject", text="1.0m")
        op05.rcg_file = "track10"
~~~

And you're done! Each button uses the same class with `bl_idname` `rcg.importobject`, but each with its own parameter value, 'track05' or 'track10' and so on.

That's all there is to it, but here are a few things that you might prefer. We can save the assignment and variable setting on two lines like this:

~~~python
        row = col.row()
        row.operator("rcg.importobject", text="0.5m").rcg_file = "track05"
        row.operator("rcg.importobject", text="1.0m").rcg_file = "track10"
~~~

A matter of taste, but I prefer it that way.

And you might wonder about using more than one parameter. You can use as many as you like, just declare them and use them in the class, and set them in the `draw` method. Like this:

~~~python
        op = col.operator("your.name", text=text)
        op.thing_one = "one"
        op.thing_two = 2
~~~

I hope you were able to find this information more easily than we did. If so, thank your search engine.