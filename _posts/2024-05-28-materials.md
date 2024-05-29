---
date: "2024-05-28-1330"
title: Blender Materials 
---

* v0.7

Here is a roughly edited transcript of a lesson in materials in Blender, for Second Life.

JR: i think i got it back. i was trying to make a split view, going to try to figure out some shader / texture / material


JR: i was thinking add a material and then open shader editor?

NS: yes. 
in each window the icon in the top left corner
is the one defining its mode
so one can always go there and change
and the splitting and joining is like in excel basically


JR: yes found that and figured out how to make the split go away. and i do not use excel :)

NS: ok
just hover over with the mouse
and select the function on the border
in the start i tried to set up special windows which was suiting me better
but over time i found that keeping the default system is much more consistent
then change view mode (windows type)
rather tan fiddling with custom view setups

JR: yes probably


JR: hm i see that texture mapping is not intuitively obvious to the casual observer

NS: no
that is a very complicated area
I highly suggest you start to use the node system for that
it is fast and very potent
and put all functions into one window
rather than a million of sun menus
sub
So you have a model now that you are happy with ?

JR: not entirely but i think it is time to learn to do things like rivets

NS: Yes

JR: so i am starting with a cube :)

NS: let take the steps which is essential for building
1) do the model you like
2) Do the UV unwrapping and the UV mapping
3) Setup textures
So before you go to texturing
you need to have a defined UV map
is not you build should be in a uniform colour
should be
Did you make unwrap of the model ?

JR: no, how do i do that?
JR: i thought i should start by making a material for it?

NS: imagine you have a 3d object
and want to apply a paper sheet around it to make a texture
it can be hard to fold a paper sheet around so it looks like no seams
look

JR: yes i understand what unwrapping does. how do i trigger it?

NS: you go to UV edit
the is a special window
UV Editing
and then when there
select the object and go in edit mode

NS: then you can see all the build
and if ti s a simple one
you can select all points in edit mode
yes
but that is Blender's default UV unwrap

NS: every object you add has a default UV setup
may not necessary work for what you like to do

JR: let's say that where i want to get to is to put a line of rivets around all the faces of my cube ...

NS: yes

JR: so i probably want a bigger UV than it made?

NS: then you can get the actual UV map
and use that as a guide to make all the bumps you need
what material have you planned to use ?
one for the metal ?

JR: i don't understand the question

NS: one for the other parts ?

JR: oh I'm not there yet, let's just texture a cube
just to learn the basics

NS: the object may be made by different structures
OK
that is very easy
because it i is by default UV unwrapped
but if not you select all the point in it
and press U

JR: ok

NS: that give you the different unwrap options
and you just use Smart UV project
which is the general form

it cuts the object into adjoining faces
so if you don't care how the texture wraps around
it is great method for most

JR: yes. i kind of remember that from before blender had these node things

NS: yes this is not nodes
the same as previous

JR: but don't you use nodes to generate your rivets?

NS: now if you like the model to split in certain parts
You can
use nodes for that
but would take you a good week for that to get working
normal we use a bump map
to do those things
just make dots in gray scale

JR: hm ok

NS: and they will appear as bumps in the texture
but let's get the cube unwrapped
say you like the lid
and the bottom
to be on their own
could be wood planks
and the the 4 sides

JR: yes i have it unwrapped in an 8x8 map
JR: like a cross in the center of the 8x8

NS: yes it is the standard
but often you like not to follow that
so you need to be able to control the unwrapping
or add seams to the build
where the unwrap splits

JR: so do i want to add seams at the top and bottom?

NS: yes just to teach you how to
a box like this
<!-- [https://gyazo.com/af537608921d6eb79d0dc0802a71ac30](https://gyazo.com/af537608921d6eb79d0dc0802a71ac30) -->

![](/assets/p1.png)

so seams are added by selecting edges
and then go to edges / mark seams
or alternatively
Ctrl E / M

JR: ok i marked a seam at the top of the cube

NS: ok then try the bottom

JR: ok did them both

JR: now do i unwrap it again?

NS: yes

JR: regular unwrap or smart?

NS: you get a little menu when unwrapping a little bar
where one can control features as distance between island
of the unwrap

JR: when i regular unwrap made a mess

NS: but the two faces top and bottom should be independent now
the sides will be a mesh probably

JR: yes a real messy one

NS: so add one seam line to one side of the box

JR: ah ok

NS: then it unwrap like a line with faces on
a band

JR: ah ok and then i can use margin to space out the separate ones

NS: yes exactly
and you can save that UV map
and take it into PS
and then add thing thereto you texture and they will be placed according to the unwrap

JR: (which i do not have) but i suppose i could draw on it with procreate or something.
JR: in what form can it be saved? just as an image?

NS: in what ever format you draw program use
blender exports all types of textures
export
so format can be anything
But that is the basic thing to do,
because as soon as yo make more difficult models - not boxes or cylinders
you run into strange mapping of the textures

JR: yes

NS: In most cases . lats say one have a metal build thing
and one to do it quick and dirty
one can just make the seams
and select all the element with a specific material
and unwrap the whole thing in one go
and if one has two materials
do the same for the other

JR: yes

NS: OK so supposed you are happy with the unwrap
time to see how textures look t it

JR: ok yes

NS: now
you have a texture you like to use ????

JR: i can use any random one really

NS: yes
so the easy one it just to use an image

JR: yes

NS: and wrap that to the box

JR: yes


JR: how do we do that

NS: Now we leave the UV editor
and go to the Shading panel
that is where we do texture setups
you have 4 main panels there
the model

JR: ok. because of whatever i did there, i have a Principled BSDF putting green on the model

NS: and to the left of it a directory
yes it uses a default

JR: yes
JR: so somewhere in the folders i would find a texture?

NS: so the whole thing should look like this
<!-- [https://gyazo.com/934ad46dfeeeb326a711fc3bba5ef4c0](https://gyazo.com/934ad46dfeeeb326a711fc3bba5ef4c0) -->

![](/assets/p2.png)

NS: now find the texture to use
and upload that

JR: into SL you mean?

NS: If you have one in SL you need to download it
you need to find a local texture in your computer to use

JR: i have a texture on my desktop, what should i do with it?
JR: i see it in the directory window

NS: yes under that
there is a texture display window
and you need the texture to appear int hat
you see 3 lines
in the top row of the window
has a option for uploading a texture

JR: The one that says View New Open?

NS: yes
Image open
next to it

JR: in the lower left panel?

JR: not the directory one?

NS: OK there is an other way
much easier
use the directory folder
to find you texture
click and drag to the window below

JR: ok tried both. anyway now i have the image

NS: Good
So you get an image
next
you need a material
and you have that green stuff
you can use in the panel to the (far) right

JR: yes the principled BSDF thing

NS: yes
so that control panel is the most confusing thing in blender
on the left side there are a lot of icons

JR: :) i agree so far :)

NS: each with different content
so you of course need to be in some window doing textures material
which is some red circle with a map on

JR: i don't see any icons on my screen or your last picture

NS: yes you doo a little (vertical) row of icons

JR: oh you mean the panel on the far right?

NS: yes
in the left side of that

JR: yes and pick the map one?

NS: there is a vertical row of icons
and you pick the one which is a red circles with something on "maybe a sphere"

JR: yes i think it is a map :)

NS: So it look like my picture
yes
so that is where one controls textures
Now to associate the image with the shader

JR: ok

NS: under the center window there is the node window

JR: yes

NS: and you have the principled shader set up
but you need a texture
so you need a node
to grab the texture and use that as colours
So in the top menu you find
ADD / texture / Image texture
should add a texture node

JR: yes done

NS: in the little box
defining the texture
there is a place called new open

JR: yes

NS: and a funny icon in front
the little icon in front
is used to select already uploaded textures

JR: ah yes picked the one from the list

NS: so click that
you get a lit of textures you  added
list
and you select the one to use

JR: and i wire color into base color and there it is

NS: exactly
and you box should be textured

JR: now when i export that to DAE will it retain that texture?

NS: no
DAE is erratic with textures
it should be possible but I've never had it work
So one upload the box as DEA no textures

JR: again in SL

NS: and the textures you used after
and then texture it is SL

JR: so given this texture can i see it on the UV and then adjust where the wrapping is?

NS: yes
we go back to the UV thing
UV editing
Here's a picture:
[https://gyazo.com/e62b473e305d1ef7369a927b2d9d5fce](https://gyazo.com/e62b473e305d1ef7369a927b2d9d5fce)

![](/assets/p3.jpeg)
here i am back in my box a bit more complex
i have it is edit mode and selected all the faces on the top
and in the right panel you see the UV MAP
and i selected an image that was used to texture
now i can decide where i like my UV map to be
maybe i like the top of the box to have the whole map
<!-- [https://gyazo.com/3c0715c29431c5461afb61fb63f0e3a7](https://gyazo.com/3c0715c29431c5461afb61fb63f0e3a7) -->

![](/assets/p4.png)
like this
and i can get my texture displayed as i like
<!-- [https://gyazo.com/58eb1c9288226b7f72b39b4ea8f4e726](https://gyazo.com/58eb1c9288226b7f72b39b4ea8f4e726) -->


![](/assets/p5.jpeg)
So if you have a special texture with things you want to display
you can fiddle the UV map around
to cover those areas

JR: Needed to set the  view to see rendered view here ?

NS: so you need to display it differently
yes you have those setting fo mesh and faces and textures
so need the textures to see those

JR: ok so i can drag theUV things around to line up with my input texture
JR: and then when i export ... and put that texture on that material ... voila

NS: yes
then you can export the model
and the texture
and when you add the texture in SL
all should be perfectly aligned

JR: yes. what was interesting is the SL showed the texture ... but did not load it

NS: no

JR: so if there were separate materials they would be faces in SL?

NS: one needs to get it separately
or you can try to add the texture upload with the model there is an option
but i have very bad experiences with that

JR: yes i tried and it is in the DAE but still doesn't come in to SL

NS: No

JR: can you sketch for me the procedure for doing a bump map? or is this enough for one day. I've used up your whole day so far.

NS: the bump map is a gray map
black is low white is up
so we can do a simple thing to get you started

JR: ok
JR: just a bump or crease or something simple

NS: OK the bump map should start out as a uniform gray colour 0.5, 0.5 0.5 RGB
So the process is to make a picture that can act as a bump map
we can do that in blender

JR: yes

NS: First let is go to the texture paint mode
the panels call textures paint
the view is called texture paint

JR: ok yes

<!-- NS: [https://gyazo.com/b51993563144c3ba47c78f823e13f6e3](https://gyazo.com/b51993563144c3ba47c78f823e13f6e3) -->


![](/assets/p6.jpeg)

JR: that still has my starting picture in it

NS: look like this for me

JR: yes exactly

NS: the first thing we need
is a new picture
in the left panel
there is a Image menu
So Image / New
and you get a new picture you can name and save
should be all black

NS: you can name it in the bar in the menu line
say bump map
"Bump Map"

NS: OK we like some bumps
on the model
so you draw a few white lines across the black image
[https://gyazo.com/97e420fb7b27b350dc319b24ad0fe44c](https://gyazo.com/97e420fb7b27b350dc319b24ad0fe44c)


![](/assets/p7.png)
like this or anything

NS: then we have created the basis for a bump map
but we cant see it on our model
So we need to associate
the bump map image
with the texture nodes
for it to display

NS: So we go back to Shading
and you add a new node

NS: from the node menu
no it is a bump node and a texture
So first the texture
add one new
and associate it with the bump map

JR: confused. do i add a texture node and put the bump map into it?

NS: No you first add the texture
it is one node
then you add a bump node
ADD( VECTOR /BUMP

JR: add image texture? i am not clear on how to add the image we just drew.

NS: [https://gyazo.com/d59b8bafc91b5107b4192819a51fd059](https://gyazo.com/d59b8bafc91b5107b4192819a51fd059)
![](p8.png)
like this
you can see in the texture
node
there is that little icon to select textures in front of the name field
so click that and select the texture

JR: i am behind. is the Europe thing an image texture node?

NS: no in the node editor window
[https://gyazo.com/a686620080b4f8574f9e2c13be0b3a2d](https://gyazo.com/a686620080b4f8574f9e2c13be0b3a2d)
![](p9.png)
like this

JR: ok i do not know how to get those two new nodes in
JR: what did you add?

NS: first i added a additional texture node
then i added a bump node
then i associated the texture node with the bump texture

JR: ok add vector bump

NS: yes
so you have two new nodes
and then the texture node
need to be associated with the bump map picture you made
so set the name to that
clicking the little icon in front of the name field and select the texture from the list

JR: ok got it

NS: ok now we like to test
so drag the colour
from the new texture node to the BSDF shader
you should display the bump picture
on your model

JR: yes

NS: 
<!-- [https://gyazo.com/c6f31b4b4132d8ac04411179964c0f89](https://gyazo.com/c6f31b4b4132d8ac04411179964c0f89) -->
![](p10.jpeg)
like this
so you are use you got th right texture

JR: yes right

NS: but you like to make it into a bump thing

JR: so wire it to height?

NS: so we drag the texture through a converter
and then from the output of the bump normal
to shader normal
and restore the  colour to the original picture
<!-- [https://gyazo.com/7c6fe382cb76d36a6f478017deedab8b](https://gyazo.com/7c6fe382cb76d36a6f478017deedab8b) -->
![](p11.png)
so i got this

JR: mine looks mostly like a dark smear across the picture

NS: can i see
your setup
a screen dump

JR: [https://gyazo.com/6651dcfb444e0abe5de9fa930e2938ca](https://gyazo.com/6651dcfb444e0abe5de9fa930e2938ca)
![](p12.jpeg)

JR: i think it's probably right just looks weird because of my weird image

NS: yes ok
it of course depends on the bump map but it is ok

JR: with a sensible texture it would look better.

NS: depends on how the light falls
how steep the side are
if you make like total black and white
it will not work so well
it is best for gradual changes in surface
but that is the very basic setup
Now
thing can get nicer
there is a little trick in Blender
you go to the node window
and click in the node with the bump map
so it get highlighted
<!-- [https://gyazo.com/ed525bdc75a91870a7bd3ad69b7c2eea](https://gyazo.com/ed525bdc75a91870a7bd3ad69b7c2eea) -->
![](p13.png)
then return to texture paint
<!-- [https://gyazo.com/85a0b995f6f9486a8e17328e93f4d9e8](https://gyazo.com/85a0b995f6f9486a8e17328e93f4d9e8) -->
![](p14.png)
and you should have this picture
where the bump map is displayed on your model
and then you can draw directly on you model
and it will be reflected in your image

JR: ah yes i see :)

NS: 
<!-- [https://gyazo.com/80a2bdcf112e6621a1e475953e8ecc22](https://gyazo.com/80a2bdcf112e6621a1e475953e8ecc22) -->
![](p15.png)

JR: white is up black is down?

NS: like this
yes
and then one can use all the paint system in blender to shape things
make grooves and lines and whatever
place dots as bumps
engrave with a gray colour and so on
but you get an idea of how the bump are placed

JR: it seems like it draws with a hole in the brush

NS: ok
so maybe you have a fun brush
to go through the option of drawing in blender it a study in itself
basically it can do anything Photoshop can do and more

JR: 
<!-- [https://gyazo.com/b39085ce6e82c92f389a045f2005aac8](https://gyazo.com/b39085ce6e82c92f389a045f2005aac8) -->
![](p16.jpeg)

NS: but it is much much more complicated
ok the whole
is the white top
you draw a white line on a black background
white will be all flat
max height
therefor a real bump map

JR: but see how there are two lines there? I just drew the one shape

NS: is starting out as a gray scale image
set to neutral 0.5 gray

JR: and it's kind of a double image

NS: because you see reflections
and shadows
and it all depends on how light affect the surface
if you have light from you viewpoint you will see nothing
no shadow
so restrict yo bum to within
the gray scale

JR: In this picture ... 
<!-- [https://gyazo.com/da68ac53eceb9a4a3a4c4ec9935434c9](https://gyazo.com/da68ac53eceb9a4a3a4c4ec9935434c9)  -->
![](p17.jpeg)

JR: I just drew one black line over neutral gray
but there are two lines on the image. i do not understand why.

NS: yes
    DS: that's the 3d view
it has to do with image resolution
and is a 3 D view
    DS: so it looks like embossing
find a softer brush
and a bigger line
<!-- [https://gyazo.com/7c7842c4e83b543c91c63b363dc02ae3](https://gyazo.com/7c7842c4e83b543c91c63b363dc02ae3) -->
![](p18.png)
the same in my example

JR: ok. how do i get a "softer brush"?

NS: [https://gyazo.com/9876b4fb9f9b3ab38e6da1c2b97ef59f](https://gyazo.com/9876b4fb9f9b3ab38e6da1c2b97ef59f)
![](p19.png)

JR: oh i just have one, i think: texdraw

NS: there is a huge system to set up brushes
with these menu headlines

JR: ah wonderful :)
JR: i suppose it can import .brush files or some such?

NS: yes that is possible too
but the best you can do
is simply not use white
use a shade fo gray
and then so to fall off
and select the fall off around the brush

JR: yes. oh before i pass out ... how did you make that round one on your example

NS: was just here
i did not select anything special for this example

JR: so that is just a single dot?
JR: ah yes i see

NS: yes

JR: well i have more than enough to start me off. this was very kind of you to walk me through all this

NS: just a single dot
and you can set dot spacing

JR: thank you very much :)

NS: and make them run at a line
and all kind of things
So the last thing we need
before ending today
is how on earth does one use that in SL
Because we have Normal Maps here
no bump maps
So we are in some small troubles
So we need to convert the bump to a normal map
Lucky the node system support that too
So lets go back to the SHADING panels
and add a new texture to the system of nodes

JR: ok

NS: i add a stand alone image texture node
<!-- [https://gyazo.com/3dbc1df0d9867d6fbc3ccbeff2c8b4df](https://gyazo.com/3dbc1df0d9867d6fbc3ccbeff2c8b4df) -->
![](p20.png)
like this

JR: ok

NS: if i press new
in the texture node
i can make a new image

JR: yes. blank?

NS: 
<!-- [https://gyazo.com/1b086690bb289a97abfbbc36a2135ade](https://gyazo.com/1b086690bb289a97abfbbc36a2135ade) -->
![](p21.png)
call it maybe normal map
you can rename it anytime
should be a blank black image

JR: and alpha on

NS: alpha off
only 3 channels
RGB
you can display it in the picture display panel
by finding it in the list
see it is a black square

JR: wait please
JR: your picture showed alpha on

NS: Yes doesn't matter
THe real thing is alpha off
Normal map doesn't have alpha channels

JR: ok so anyway i get a black thing by opening the normal map on the left

NS: you got it?

JR: i think so

NS: super
So next thing is to bake a normal map from what we have
the material node system we created

JR: ok. ready. :)

NS: So go to the node panel
ensure the Normal map texture is highlighted
then go to the RIGHT side panel

JR: yes

NS: 
<!-- [https://gyazo.com/356757e975f99b48e9ce42e95bcae37c](https://gyazo.com/356757e975f99b48e9ce42e95bcae37c) -->
![](p22.png)
go to the near top
and click the render icon
and select the render mode to cycles

NS: now scroll down tot he bottom of the panel
you find a entry called bake


NS: 
[https://gyazo.com/544fa82faec8cf7965107102d70223c7](https://gyazo.com/544fa82faec8cf7965107102d70223c7)
![](p23.png)
looks like this when opened

NS: you have to change the bake type
in the top of the menu
to normal
<!-- [https://gyazo.com/200280b78553b08e970acd34982c5980](https://gyazo.com/200280b78553b08e970acd34982c5980) -->
![](p24.png)
and then scroll down
n just press bake
the button bake
you will get an error if no object is selected
then select the cube in object mode and try again

JR: i do not see a bake button

NS: it is on the very top
gray bar call bake int he bake menu
the very top thing
above where you set the bake type
<!-- [https://gyazo.com/85d26a98ff9ae7c719600389c033c0a8](https://gyazo.com/85d26a98ff9ae7c719600389c033c0a8) -->
![](p25.png)

JR: ok it slowly did something
JR: over in the image window

NS: yes it may toke some time
and the image window

JR: kind of looks like the other one
JR: but colored

NS: yes bluish

JR: yes

NS: 
<!-- [https://gyazo.com/0510706d8fd850f4ca8c9d5267ecbf10](https://gyazo.com/0510706d8fd850f4ca8c9d5267ecbf10) -->
![](p26.png)
like this
something
that is the normal map

JR: yes

NS: Now if you have a more complicated setup
you may bake a lot of normal maps same time

JR: do i wire it into the diagram?

NS: NO you save it as a picture

JR: let's stick with simple for now, my brain is full :)

NS: called something like JR_Normal
Just save it
and then upload to SL

JR: ok how how do i save it?

NS: In the texture window where you see it
you can click the icon with 3 horizontal line
there is a save image operation
will save the picture on display
best to save as PNG

JR: yes got it

NS: Super then upload
to SL


JR: ah got it

NS: smiles
ok then you need to add it to the texture on your SL object
as a normal map

JR: is that bumpiness or shininess

NS: bump

NS: but that is the principle
when one is only using blender to do it

JR: super. i am so grateful for this help

NS: yes

JR: it should get me started

NS: smiles