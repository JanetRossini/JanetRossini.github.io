---
date: "2024-06-26-0720"
title: Texturing
---

NS: So a new blender  session

DS: ok
NS: I  think we shoudl start  with a  cube
NS: as always
DS: ok
NS: and a  good way  will be to add a  texture
NS: So let me  just  find soemthign  usefull
DS: ok
DS: you can pass it via SL and we can download it
NS: ok just to make  thign a  bit  different  today
NS: we star t out  with a  cube
NS: and the  add a metal  surface
NS: lol  try to find a  asimple  texture
DS: did you find turning down the render number helped janet?
JR: i'm not sure
NS: there si a  texture calld raw  iron
JR: raw iron
NS: raw iron
DS: in blenderkit?
NS: yes
NS: in  blender kit
NS: pretty  simple  node  structure
NS: and  4  different
NS: textures
JR: ok got it
DS: me too
NS: ok  so we ara ll aligned
NS: let  look at the  noce tree first
NS: node tree
JR: base metallic roughness normals
NS: we see the  colour and  roughness
NS: metalic
NS: and then there is a  normal
JR: yes
NS: and a displacement thing
NS: the  Displacement is  nto  usefull for  SL
NS: it can be there
NS: whispers: which is  ok  but  can not be  used in SL
JR: ok
NS: So what we like to  do
NS: is  to change the  Normal map
NS: and change how  the  normal map  behave
NS: here si  oen node  we can  use to add an addition normal map
NS: called BUMP
NS: https://gyazo.com/10d235a2d4823dfc6d33f79c1a89e35a
JR: yes
NS: So try  to get that to the  node system
NS: and insetr  between the  normal output of the  normal map
NS: and the  normal input  to the  principal shader
NS: https://gyazo.com/ad205e1f8c3575f0fdd5e47f8ce27113
NS: like  this
DS: how do we find it
NS: you  clcik on add
NS: add a noce
NS: node
NS: when the  first  list appear you can type  in bump
JR: got it
NS: else  it is  a vector  noce
DS: ok
NS: so Add/Vector/Bump
DS: wondered how to search
NS: yes  to search  just clik on the  node selector  and  type
JR: i do shift-a to add the space takes me to search
NS: Yes  janet
DS: ok
DS: done
NS: there is  unfortunately many strange thign in blender still Space starts animations for me
NS: Ok we loook at the  node
NS: and there is  some input called hight
NS: Hight is a  gray tone immage
DS: ok
NS: that is  tranformed into normals
NS: So what we can do now
NS: is tomake a texture
NS: that will be the  bump needed
DS: ok
NS: to do that
NS: we need first a proper input related to the  UV map we use
NS: so the  textures are aligned
DS: ok
NS: So let us add a  Image texture
NS: Add /  Texture / Image
DS: ok
NS: https://gyazo.com/eb76e49ff6d0ecca158473eec9cc19d9
NS: somethign liek this
NS: So we have to connect that into the node tree
NS: The input should be the same scaling as the  uther textures
NS: they all are fed with a  vector  input  from mapping
NS: so we simply connect  that  to the  vector  input of the  texture
DS: ok done
NS: and then the  colour  input
NS: goes into the  hight of the bump noce
JR: wait connect what to what?
NS: https://gyazo.com/d4006b02bb99c2b162d119afa6ed7937
NS: you need aninput  witch is  the  vector (UV) map  intomation
NS: and the output  goes into the  hight  of the  bump  node
DS: color output of image to height of bump
NS: yes
NS: So we added a  extra layer of normal mapping
NS: on top of  what was there originally
JR: ok i have it
DS: mee too
NS: Ok
JR: so this is what, feeding in a blank black texture just now?
NS: Yes next is  to make a  actual texture
NS: we are fortunate
JR: how nice
NS: the  Texture noce has a new  function
NS: So one can click  that
NS: and then define an image
NS: no alfa will be best
JR: size 1024 and blank ok?
NS: yes
NS: https://gyazo.com/755da268010151523783828eb6c8c5ec
NS: and there si s a colour setting too
NS: has to be non-colour
JR: i don't understand that last image
NS: Colour Space - non colour
NS: ts is  how  i added a  texture
NS: i called it  bump
NS: and i canged the  colour Space to non colour
DS: ok
NS: It is  hight measurement not a  colour
DS: done
NS: we add to the  thing
NS: So with  this  setup
NS: we can start  to change the  Normal map
NS: by  painting on the  texture we added
JR: ok ... so far i feel like i'm working without a net
DS: we will draw that soon :)
NS: Yes Janet
NS: Sorry for the  complexity
NS: But we arr all there
NS: Have a bump  node
NS: with an associated image
JR: somewhere
NS: and changing  gray  tones in that
NS: chould change the  normal map
NS: add or  subtract from it
DS: so this is useful for rivets?
NS: Yes it is  usefull for  anything
NS: I  will come to all the  options
JR: ok
DS: embossing in metal
JR: i have the bump defined and linked
NS: but  here the  important  thign is  the  way to add  the  bumpmap
JR: but no image yet
DS: same here
NS: You shoudl  have a  back image in the  Image display called  "bump" maybe
NS: if you go to the  side  panel
NS: with is the  image display
DS: yes
NS: you shoudl have a pictuure with the name you gave
NS: and it  si  by default  black
DS: yes
JR: i see an 8x8 square with no name
DS: https://gyazo.com/6be978f905d143ea097915e692d5c44d
NS: ok Janet
DS: i had to find it in the dropdown
NS: yes one need to  find it  in dropdown
JR: ok that was the secret step
JR: now i have a black thing, very large
DS: :)
DS: yes
NS: always  hidden layers in blender
NS: Smiels
NS: sow e are pretty  well off
NS: to make the  first  bump map changes
NS: No  we have an image
NS: and we like to change that
NS: in order to do that
JR: ok black square
NS: we need to  go to a new setup
NS: Called Image paint
NS: sorry texture Paint
NS: "TEXTURE APAINT
NS: Before ve do
DS: ok
NS: it is  cruciial  that we have selected the  image  we like  to change
DS: ok
JR: jump from plane.
DS: :)
JR: before jumping from plan, be sure you are wearing your chute.
NS: So you have to click  in the  node tree
NS: on the bump map  image
NS: so it  get a  highlighted border
DS: ok
NS: then when you go  to  texture paint
NS: that is the  image  you  work on
DS: ok
JR: ok
JR: seems right. says bump. i see  black ckube
NS: Ok  so my  window looks like this
DS: https://gyazo.com/1c7164898987625c5b61f5d4925346a6
JR: yes
NS: https://gyazo.com/09c7349b5b4a04e7a500dfa3f84bc712
DS: ok
NS: we have a image  display
NS: and we have the  cube
NS: one can change the  way  ti is  shown
NS: using the  icon inthe  upper  right  corner
NS: as in the  model  window
NS: show  ti as a  mesh  or  with  fidderent  textures
NS: the  best here is  to show  in  full render
NS: https://gyazo.com/ab227bbe8d7e7a08b1767fbe528c998a
DS: oki i hade to open the veiwport wide to see that
NS: yes
NS: some miht  be  hidden
NS: So now  we  are in a  texture draw mode
JR: yes that is odd
JR: ok yes
DS: yes
DS: 2
NS: and in the  texture panel
NS: one can draw
NS: as example  some  white line
DS: (moves blender to Huion screen)
JR: what brush should we use?
NS: So if one pla  with the  Display
NS: on can switch
NS: between different modes
JR: i just have the one i guess texdraw
NS: Se ejust the  texture
NS: or the  full render
JR: ?
DS: https://gyazo.com/9306dad08d43a09189b9b7b8f22cbcbc hehe
NS: https://gyazo.com/b85953c3d8c28897d29735024d242342
NS: my  thing  in texture mode
NS: and we can see the  UV is  repeated many  times
DS: the brush size is [ and ]
DS: like in PS
DS: and CSP
NS: yes
JR: mine is not changing the picture
JR: https://gyazo.com/05f3868b2e33842f347e1a7a4d3627a9
NS: Janet
NS: I  think i  made amistake
NS: mistake
NS: int he  node tree
JR: ok
NS: https://gyazo.com/1b73c7a78872a9db6e594c09dd312b2b
NS: the  bump map  picture has to be  inputted to the  hight
NS: like shown here
NS: Sorry  (mistakes happens)
NS: int he  end
JR: ah yes much better
JR: :)
NS: we shoudl see somethign liek this
DS: i made a mistake and connected it
NS: good  Dizzi
NS: Also make more sence
NS: sense
NS: so we see anythign we draw
NS: on the  picture is  nor refleced in a change fo the  normal  map
NS: So
NS: Now we need to knwo  abit of how th e bump map  are jandeled
NS: handeled
NS: gray  128   is no change
NS: and more white  is  up
NS: darker is  down
NS: So the  normal  way to do  a bump map
NS: is  to make  it  uniform gray
NS: and the add hight or  dept
NS: so  just colour pick a  mid  gray tome  and
DS: so set grey and a big brush and paint it all?
NS: then paint the picture with a  huge  brush
NS: make it all gray
JR: i have a question
NS: yes
NS: Yes Janet ?
JR: i was drawing in white, as i think you were, and got the pattern on the cube as you had (I think)
NS: yes
JR: then i tried to erase it and painted all in black ...
NS: yes
JR: and the pattern does not go away even tho the texture looks black
NS: and it  vanished
DS: IT SEEMS TO PAINT IN MULTIPLY
DS: sorry
DS: i had to go over several times
JR: ah blending mode
DS: had to go over 10 times
NS: it is  like photoshop
NS: with  diferent  way  to  mic  brushes
DS: yes it was in mix
NS: mix
DS: yes i understand that
NS: I think the  main thign here
JR: nothing i do seems to make it go away
NS: is one can get to the  texture paint
NS: and get the  right  texture selected
NS: and actually see how  one  cange the  bumpmap
NS: But we are not  done
NS: ecause  we have  even more poverfull tools  here
NS: One can draw ont he  cube  directly  too
NS: and it  wil change the  image  selected nothing  else
NS: So if we all make the  image  grayish
JR: nothing i do affects the cube
NS: Ok Janet
NS: So did  you  fix the little thing with the  node tree
NS: https://gyazo.com/c92f59f240db9c339ddec326b5bc9723
JR: yes and i have the crosshatch but that is now all i can get even if i paint more
NS: colout input  from the texture  has to go into the hght
JR: https://gyazo.com/e054eb0c4817d6488e412e3865653f6a
NS: Ok  so go back to the node tree
NS: ok that might  be  ok  Janet
NS: try to  make a  unifor colour in grqay  all over the  image
JR: https://gyazo.com/1004573d08c659ad65c176c5177662dc
NS: nodes are fine
NS: so  if w e get the  image  in a  gray  tone  unifor all hight  changes shoudl vanish
JR: now it did this https://gyazo.com/3240d485f72c66a976dbe0fc9e7baff5
NS: smiles
NS: are yo sure you  ahve the  right  image  selected
NS: int he texture paint
NS: there si  somethign  makign bumps
DS: try going over the area a few times
DS: it took 10 passes for me to flatten it
NS: set the  strength  to 100
NS: of the  brush
DS: and i could not see the lines in the texture
JR: max strength is 10
DS: maybe why i had to pass over 10 times
NS: For now  no not  change the  node settings  janet
JR: i am not changing any node settings
NS: can you  give us a  picture fo the  full screen
DS: its the brush
NS: so we can see the  selections meny bars
JR: https://gyazo.com/a47c1752ba578e8c2b7710d25c3e3504
DS: set the radius large and scrubb the area a lot
DS: down to grey
DS: and watch the stuff in the 3d window
DS: see it the scratches get less
NS: An other  thing might  to try to save the  bump  image
DS: i had to scrub the window 10 times before the brush cleaned the previos
JR: i have been scrubbing and scrubbing
DS: ok
NS: Try  to save the  Bump immage
NS: to the  drive
JR: how does one do that
NS: Sometimes bender do not  update  if there is not  file to save to
NS: Click in the minu  on image
NS: and save
NS: or save as
JR: k done
JR: that cleared it
JR: sheesh
NS: yes
NS: sorry  ti is a  old Blender  problem
JR: sorry for the delay.
DS: np
NS: took me  tons of  frustration
DS: explains why it happened here too
NS: and headace to find what i  lost
NS: But we gt a  logn  way
NS: we have a  texture with  can be a bump map
NS: and can paint on that
NS: Next
DS: https://gyazo.com/dd897a348a539b87bd6444bc042af944
NS: Now we have  cleared the  bump map
NS: we can go the  the  image  display  window
NS: and then draw dirctly on the  cube
DS: yes
NS: wotks  the  same  waqy
NS: way
DS: :)
NS: and one can add doth and critical thign to the  3d model
JR: bah
JR: now it is stuck flat
NS: yes
NS: so you  got all flat again  janet
NS: then try to  so to the  model  window
NS: and use the  brudh there
JR: and nothing i draw in the square or on the cube makes any difference
JR: whether i draw in black or white
NS: mmmmmmmmmmm
DS: what colour pen?
DS: ok
NS: ok that is  odd
JR: ok i saved the file andn reopened ad now:
DS: and worked?
NS: Ok
NS: it  shoudl be  dynamic
JR: oh wait not in cycles
DS: im in evee
NS: ok that  may  explain
JR: fuck me. which are we supposed to be in?
DS: cycles i think
DS: i forgot
NS: yes try  cucles
NS: Eevee shoudl show  bump map  too though
JR: now i have this: https://gyazo.com/3487b0685bab56e84d361211c29a3cbb
DS: it did
NS: ok that is  fine  Janet
NS: then you have to select a better display
NS: it is  the  icons in the  upper corner
JR: yes it lost that setting
NS: whare you select  between  mesh  faces texture or  full render
DS: yes was like this https://gyazo.com/b81a36d7ff89cf415f9bcde208a3087c
NS: https://gyazo.com/a0623dc2b7b45cff17c0669b6da0aea0
NS: you can  swith  to see  the  textur  onthe  onject or the  render of all
NS: you see the  texture directly
Eye of Odin HUD to wear: + LibbyCoker  [4]
Eye of Odin HUD to wear: - LibbyCoker  [3]
NS: Actually i think it  works best in eeevee
NS: EEVEE
DS: yes its less grainy
NS: yes and  faster update of the  bump
NS: But we need to get Janet in line
JR: again i cannot draw
NS: Ok Save the  file
NS: close the  all
NS: then reopen
NS: you  shoudl get back to  whare you are
DS: yes but you could draw this externally in Procreate or PS
JR: i yes but still cannot draw on the image or cube
DS: ok
DS: i see
NS: So try  to close it  Janet
NS: somethign got  stuck
JR: closed and reopened blender still nothing
NS: then reopen the  blender file
NS: whispers: and you can not  draw ont he  image ????
JR: i can draw in white on gray but not black
DS: these are my brush settings https://gyazo.com/3288e82a973b80f5751cda17136c53d2
NS: Shoud draw  thing  white lines
NS: thin
NS: white lines
DS: yes
DS: it does
JR: it's sort of working now
JR: no idea what changed
DS: yes?
JR: anyway i think i understand up to now what should be possible
NS: Ok se we have  to align again
NS: we all make the  immage  a gray tone
NS: and bump  should  vanish
NS: then we can  go to the  model  window
NS: and try t make  bump  by  direct draw ont he  cube
NS: make some dots around
NS: somethign liek this
NS: https://gyazo.com/fd060fd2497d4e12ab40b86b4a3dc1ce
NS: it shoudl change the  image
NS: relecting the  change
NS: reflecting the  changes
NS: You got that ?
JR: shouts: yes i managed to get something like rivets. but you have to paint a lot to get it flat again. perhaps best to start with new textures
JR: sorry
NS: Smiles
NS: Ok Janet
NS: as long we have  some  dots
DS: yes im seing same sort of stuff, why not make a texture in 128 grey and load it before scrawling on it
NS: one can  do that
NS: it  takes me 2 strokes to go gray
NS: make a brush 1000 pt
DS: ok
NS: and then 1000 percent
DS: https://gyazo.com/781583771e447083de4382c492d630ba
NS: and it  delete all
DS: where is the 1000% ?
NS: Sorry strength 10000
NS: 1.0000
DS: ok
NS: full strength and mix
NS: overwrite what is there
DS: yes
NS: We all have  dots
NS: Janet  you got  some
DS: ill try wiping what i have clean then
NS: Ok  Dizzi
JR: now i can draw in the texture and not on the cube. wtf.
NS: then save texture  janet
DS: wiped clean still bumpy
DS: https://gyazo.com/98e7368eaacefb95de466d99d0f6c73f
NS: yes it is nto  clean Dizzi
NS: But before we all get totally  frustrated
DS: took 5 passes
DS: yes
NS: Please make some  dots of some kind
DS: ok
NS: and tell me if  you have
DS: https://gyazo.com/446c2dc5c49530aba534260ebd043671
NS: good  Dizzi
JR: https://gyazo.com/0fb02ef4cd832b2693d9e754b57dde45
NS: good Janet
NS: Ok
DS: :)
NS: The strength of the bumpmap
JR: i think i get the idea but i have no clue why it works sometimes and not others
NS: the  power  how  ti is  displayed
NS: is determined int he node tree
NS: and that si  important to know that once can change the  strength
NS: we  run  on  a  huge amplification
NS: so we  go back to the shader editir
NS: editor
NS: find the bump  node
NS: and notice there is a  strength setting
NS: it is  by default set to  1.000
DS: yes
NS: not try to change  to  0.1
NS: reduce by  10  times the  strength
JR: ah it is range 0-1
DS: https://gyazo.com/e28ccef593bd1afb5cdd1d22e533510d
NS: yes and one can tyne the effect of the   bumpmap
NS: sliding it  up and  down
NS: one can also play  with the  distance
NS: it is  usuallt  set to 1 and keept  fixed
DS: what does it do?
NS: usually
NS: it compress the  information in the  bumpmap  picture
NS: if the strength is  1
DS: ok
NS: light gray  is already out of  range
NS: and  Black is  out of  range
NS: so you get  jetky  bumpmaps
NS: with flat tops and growes
DS: ok
NS: So  one  have to  tune the bumpmap  into a proper range
NS: It also means
DS: so leave at 1?
NS: one are more free to  draw the  bumpmap
JR: i suppose there is some way to create more than one and use them?
NS: Strength  is about  0.1 - 0.3 maybe
NS: Distance  keep  on  1
DS: ok
NS: Ok
NS: so what we have  now
NS: is some controll of  how a  bumpmap will affect the  model
JR: yes, and i crave a break :)
JR: but i think i mostly get the idea
NS: Yes  ajnet  Lol
DS: :)
NS: Next will eb  makign an external bump map
NS: will be  much the  same
DS: so basically how do we get this into SL?
NS: that  ahs  to be  baked
NS: has
DS: next lesson
NS: One  bake the normal map
DS: save what we have?
JR: i'm sorry, i must log and undertake the bins.