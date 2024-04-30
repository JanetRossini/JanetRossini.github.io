---
date: "2024-04-29-0646"
title: Initial Add-On
---

Today, with the help of ChatGPT, I plan to try to build a very simple add-on and get it to work in Blender via the standard add-on path. I am torn about using ChatGPT. Since I started trying it a week or so ago, it has been giving me very useful information, much more easily than I can get it even with my surely above-average search skills. (It is not always right, but it is good about trying again.)

My concerns with LLMs like CharGPT are many: They're already being used in places where they're potentially dangerous. They have already begun to displace some human workers. They consume large amounts of energy, which is not good for the climate. And they are enriching some people who are already more rich than anyone deserves.

I tell myself that as a professional, I need to understand these things, and that I will stop using them soon, once I am well informed. I'm not sure I believe myself, and for sure ChatGPT has been very useful. We'll see some of its answers in this article.

I'm going to create a new PyCharm project to hold my simple add-on. When it works, if it works, then I'll use what I've learned to create the real one that we need.

## The Next Day ...

I spent more hours than I'd have liked to, to get a simple add-on running. Along the way, the only way I found of getting a PyCharm multi-file add-on to work was to zip up the folder containing the project, and add that in the add-on Install dialog. (I have read that when Blender 4.2 comes along, what I am doing here may need to be done with "install legacy". I don't know any more than that, but this hint may come in useful for someone someday.)

I created a simple add-on according to the [Blender 4.1 Add-on Tutorial](https://docs.blender.org/manual/en/latest/advanced/scripting/addon_tutorial.html#add-on-tutorial). Originally I had it in a file named `simple_addon.py`, and in that form it would add and run. But for a multi-file version, we need an `__init__.py` file, and whatever imports are necessary to make it all hook up, which was what I was here to discover.

I posted an [inquiry on Blender.stackexchange.com](https://blender.stackexchange.com/questions/317388/multi-file-add-on-cannot-find-import), and a kind soul mentioned zipping the folder and adding that, and that got me on the way.

Skipping to the current situation here is the project structure:

~~~
my_addon/
│
├── __init__.py
├── simple_operator.py
└── panels/
    ├── __init__.py
    └── simple_panel.py
~~~

And the files. The top-level `__iniit__.py`:

~~~python
bl_info = {
    "name": "My Addon",
    "blender": (2, 80, 0),
    "category": "Object",
}

# if "bpy" in locals():
#     import importlib
#     if "my_operator" in locals():
#         importlib.reload(my_operator)
#     if "my_panel" in locals():
#         importlib.reload(my_panel)
# else:

import bpy
from .panels.simple_panel import SimplePanel
from .simple_operator import SimpleOperator


def register():
    bpy.utils.register_class(SimplePanel)
    bpy.utils.register_class(SimpleOperator)


def unregister():
    bpy.utils.unregister_class(SimplePanel)
    bpy.utils.unregister_class(SimpleOperator)


if __name__ == "__main__":
    register()
~~~

The commented bit is something that I think we'll need for reloading to work, and is there to remind me of the need. At that time, I think we also need to put the imports right below inside the else. The idea, as I understand it, is that when you reload, `bpy` will be defined and so you reload the stuff, but when you are loaded initially, `bpy` is not defined and you do the imports. This is arcane magic to me, but I think we'll need to know it someday.

Aa this stands, if we had 87 files in the add-on (please, no), we'd have 87 imports, register lines, unregister lines. We'll be working on a better way to do that. 

The inner `__init__.py` is empty, just there to signal "package" to Python. It may not be necessary, but since I am just following instructions here, I included it.

Here is `simple_operator.py`:

~~~python
import bpy

class SimpleOperator(bpy.types.Operator):
    """Tooltip for Simple Operator"""
    bl_idname = "object.simple_operator"
    bl_label = "Simple Operator"

    def execute(self, context):
        # Operator logic goes here
        print("Simple Operator executed")
        return {'FINISHED'}

def register():
    bpy.utils.register_class(SimpleOperator)

def unregister():
    bpy.utils.unregister_class(SimpleOperator)
~~~

And `simple_panel.py`:
~~~python
import bpy

class SimplePanel(bpy.types.Panel):
    """Tooltip for Simple Panel"""
    bl_idname = "OBJECT_PT_simple_panel"
    bl_label = "Simple Panel"
    bl_space_type = 'VIEW_3D'
    bl_region_type = 'UI'
    bl_category = 'Tools'

    def draw(self, context):
        layout = self.layout
        layout.operator("object.simple_operator", text="Execute Simple Operator")

def register():
    bpy.utils.register_class(SimplePanel)

def unregister():
    bpy.utils.unregister_class(SimplePanel)
~~~

The convention I'm following is that every separate component that needs registration includes its own `register` and `unregister` functions. In the fullness of time, during the top-level `register` or `unregister`, I propose to inspect all the files in the project and if they implement those functions, call them. Until then, we simply have to list them up in the top level init.

## Installing the Add-on

With the code in place and saved, I go to a file browser and zip up the entire project into a zip file. Then, in Blender, Command+comma gets me the Preferences (also under Edit), and selecting Add-ons gets me here:

![ready to add on](/assets/ready.png)

Click "Install", navigate to the zip file, select it and install. That should bring you to this picture:

![ready to enable](/assets/enable.png)

Click the little checkbox to enable your add-on, and you should be good to go.

If there is something wrong in your structure, trying to enable may produce an error message. At this writing, all I can really recommend is that you adhere closely to the structure shown here, and make very small changes away from it, so that it is easy to revert when something doesn't work. In subsequent articles, I'll try to build up enough understanding so that I can at least try to explain it.

What I know right now is that it works on my machine. :)

Progress, and I am happy.