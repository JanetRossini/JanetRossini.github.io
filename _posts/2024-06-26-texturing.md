---
date: "2024-06-26-0720"
title: Texturing
---

[2024/06/26 11:26]  NightShade Fugu: So a new blender  session
[2024/06/26 11:26]  Dizzi Sternberg: ok
[2024/06/26 11:26]  NightShade Fugu: I  think we shoudl start  with a  cube
[2024/06/26 11:26]  NightShade Fugu: as always
[2024/06/26 11:26]  Dizzi Sternberg: ok
[2024/06/26 11:26]  NightShade Fugu: and a  good way  will be to add a  texture
[2024/06/26 11:27]  NightShade Fugu: So let me  just  find soemthign  usefull
[2024/06/26 11:27]  Dizzi Sternberg: ok
[2024/06/26 11:28]  Dizzi Sternberg: you can pass it via SL and we can download it
[2024/06/26 11:28]  NightShade Fugu: ok just to make  thign a  bit  different  today
[2024/06/26 11:28]  NightShade Fugu: we star t out  with a  cube
[2024/06/26 11:28]  NightShade Fugu: and the  add a metal  surface
[2024/06/26 11:30]  NightShade Fugu: lol  try to find a  asimple  texture
[2024/06/26 11:30]  Dizzi Sternberg: did you find turning down the render number helped janet?
[2024/06/26 11:31]  Janet Rossini: i'm not sure
[2024/06/26 11:31]  NightShade Fugu: there si a  texture calld raw  iron
[2024/06/26 11:31]  Janet Rossini: raw iron
[2024/06/26 11:31]  NightShade Fugu: raw iron
[2024/06/26 11:31]  Dizzi Sternberg: in blenderkit?
[2024/06/26 11:32]  NightShade Fugu: yes
[2024/06/26 11:32]  NightShade Fugu: in  blender kit
[2024/06/26 11:32]  NightShade Fugu: pretty  simple  node  structure
[2024/06/26 11:32]  NightShade Fugu: and  4  different
[2024/06/26 11:32]  NightShade Fugu: textures
[2024/06/26 11:32]  Janet Rossini: ok got it
[2024/06/26 11:32]  Dizzi Sternberg: me too
[2024/06/26 11:33]  NightShade Fugu: ok  so we ara ll aligned
[2024/06/26 11:33]  NightShade Fugu: let  look at the  noce tree first
[2024/06/26 11:33]  NightShade Fugu: node tree
[2024/06/26 11:33]  Janet Rossini: base metallic roughness normals
[2024/06/26 11:33]  NightShade Fugu: we see the  colour and  roughness
[2024/06/26 11:33]  NightShade Fugu: metalic
[2024/06/26 11:34]  NightShade Fugu: and then there is a  normal
[2024/06/26 11:34]  Janet Rossini: yes
[2024/06/26 11:34]  NightShade Fugu: and a displacement thing
[2024/06/26 11:34]  NightShade Fugu: the  Displacement is  nto  usefull for  SL
[2024/06/26 11:34]  NightShade Fugu: it can be there
[2024/06/26 11:34]  NightShade Fugu: whispers: which is  ok  but  can not be  used in SL
[2024/06/26 11:34]  Janet Rossini: ok
[2024/06/26 11:34]  NightShade Fugu: So what we like to  do
[2024/06/26 11:34]  NightShade Fugu: is  to change the  Normal map
[2024/06/26 11:35]  NightShade Fugu: and change how  the  normal map  behave
[2024/06/26 11:35]  NightShade Fugu: here si  oen node  we can  use to add an addition normal map
[2024/06/26 11:35]  NightShade Fugu: called BUMP
[2024/06/26 11:36]  NightShade Fugu: https://gyazo.com/10d235a2d4823dfc6d33f79c1a89e35a
[2024/06/26 11:36]  Janet Rossini: yes
[2024/06/26 11:36]  NightShade Fugu: So try  to get that to the  node system
[2024/06/26 11:36]  NightShade Fugu: and insetr  between the  normal output of the  normal map
[2024/06/26 11:37]  NightShade Fugu: and the  normal input  to the  principal shader
[2024/06/26 11:37]  NightShade Fugu: https://gyazo.com/ad205e1f8c3575f0fdd5e47f8ce27113
[2024/06/26 11:37]  NightShade Fugu: like  this
[2024/06/26 11:37]  Dizzi Sternberg: how do we find it
[2024/06/26 11:38]  NightShade Fugu: you  clcik on add
[2024/06/26 11:38]  NightShade Fugu: add a noce
[2024/06/26 11:38]  NightShade Fugu: node
[2024/06/26 11:38]  NightShade Fugu: when the  first  list appear you can type  in bump
[2024/06/26 11:38]  Janet Rossini: got it
[2024/06/26 11:38]  NightShade Fugu: else  it is  a vector  noce
[2024/06/26 11:38]  Dizzi Sternberg: ok
[2024/06/26 11:38]  NightShade Fugu: so Add/Vector/Bump
[2024/06/26 11:39]  Dizzi Sternberg: wondered how to search
[2024/06/26 11:39]  NightShade Fugu: yes  to search  just clik on the  node selector  and  type
[2024/06/26 11:39]  Janet Rossini: i do shift-a to add the space takes me to search
[2024/06/26 11:39]  NightShade Fugu: Yes  janet
[2024/06/26 11:39]  Dizzi Sternberg: ok
[2024/06/26 11:40]  Dizzi Sternberg: done
[2024/06/26 11:40]  NightShade Fugu: there is  unfortunately many strange thign in blender still Space starts animations for me
[2024/06/26 11:40]  NightShade Fugu: Ok we loook at the  node
[2024/06/26 11:40]  NightShade Fugu: and there is  some input called hight
[2024/06/26 11:40]  NightShade Fugu: Hight is a  gray tone immage
[2024/06/26 11:40]  Dizzi Sternberg: ok
[2024/06/26 11:40]  NightShade Fugu: that is  tranformed into normals
[2024/06/26 11:41]  NightShade Fugu: So what we can do now
[2024/06/26 11:41]  NightShade Fugu: is tomake a texture
[2024/06/26 11:41]  NightShade Fugu: that will be the  bump needed
[2024/06/26 11:41]  Dizzi Sternberg: ok
[2024/06/26 11:41]  NightShade Fugu: to do that
[2024/06/26 11:41]  NightShade Fugu: we need first a proper input related to the  UV map we use
[2024/06/26 11:42]  NightShade Fugu: so the  textures are aligned
[2024/06/26 11:42]  Dizzi Sternberg: ok
[2024/06/26 11:42]  NightShade Fugu: So let us add a  Image texture
[2024/06/26 11:42]  NightShade Fugu: Add /  Texture / Image
[2024/06/26 11:43]  Dizzi Sternberg: ok
[2024/06/26 11:43]  NightShade Fugu: https://gyazo.com/eb76e49ff6d0ecca158473eec9cc19d9
[2024/06/26 11:43]  NightShade Fugu: somethign liek this
[2024/06/26 11:43]  NightShade Fugu: So we have to connect that into the node tree
[2024/06/26 11:43]  NightShade Fugu: The input should be the same scaling as the  uther textures
[2024/06/26 11:44]  NightShade Fugu: they all are fed with a  vector  input  from mapping
[2024/06/26 11:44]  NightShade Fugu: so we simply connect  that  to the  vector  input of the  texture
[2024/06/26 11:44]  Dizzi Sternberg: ok done
[2024/06/26 11:44]  NightShade Fugu: and then the  colour  input
[2024/06/26 11:45]  NightShade Fugu: goes into the  hight of the bump noce
[2024/06/26 11:45]  Janet Rossini: wait connect what to what?
[2024/06/26 11:45]  NightShade Fugu: https://gyazo.com/d4006b02bb99c2b162d119afa6ed7937
[2024/06/26 11:45]  NightShade Fugu: you need aninput  witch is  the  vector (UV) map  intomation
[2024/06/26 11:46]  NightShade Fugu: and the output  goes into the  hight  of the  bump  node
[2024/06/26 11:46]  Dizzi Sternberg: color output of image to height of bump
[2024/06/26 11:46]  NightShade Fugu: yes
[2024/06/26 11:46]  NightShade Fugu: So we added a  extra layer of normal mapping
[2024/06/26 11:47]  NightShade Fugu: on top of  what was there originally
[2024/06/26 11:47]  Janet Rossini: ok i have it
[2024/06/26 11:47]  Dizzi Sternberg: mee too
[2024/06/26 11:47]  NightShade Fugu: Ok
[2024/06/26 11:47]  Janet Rossini: so this is what, feeding in a blank black texture just now?
[2024/06/26 11:47]  NightShade Fugu: Yes next is  to make a  actual texture
[2024/06/26 11:47]  NightShade Fugu: we are fortunate
[2024/06/26 11:48]  Janet Rossini: how nice
[2024/06/26 11:48]  NightShade Fugu: the  Texture noce has a new  function
[2024/06/26 11:48]  NightShade Fugu: So one can click  that
[2024/06/26 11:48]  NightShade Fugu: and then define an image
[2024/06/26 11:48]  NightShade Fugu: no alfa will be best
[2024/06/26 11:49]  Janet Rossini: size 1024 and blank ok?
[2024/06/26 11:49]  NightShade Fugu: yes
[2024/06/26 11:49]  NightShade Fugu: https://gyazo.com/755da268010151523783828eb6c8c5ec
[2024/06/26 11:49]  NightShade Fugu: and there si s a colour setting too
[2024/06/26 11:49]  NightShade Fugu: has to be non-colour
[2024/06/26 11:49]  Janet Rossini: i don't understand that last image
[2024/06/26 11:49]  NightShade Fugu: Colour Space - non colour
[2024/06/26 11:50]  NightShade Fugu: ts is  how  i added a  texture
[2024/06/26 11:50]  NightShade Fugu: i called it  bump
[2024/06/26 11:50]  NightShade Fugu: and i canged the  colour Space to non colour
[2024/06/26 11:50]  Dizzi Sternberg: ok
[2024/06/26 11:50]  NightShade Fugu: It is  hight measurement not a  colour
[2024/06/26 11:50]  Dizzi Sternberg: done
[2024/06/26 11:50]  NightShade Fugu: we add to the  thing
[2024/06/26 11:50]  NightShade Fugu: So with  this  setup
[2024/06/26 11:51]  NightShade Fugu: we can start  to change the  Normal map
[2024/06/26 11:51]  NightShade Fugu: by  painting on the  texture we added
[2024/06/26 11:51]  Janet Rossini: ok ... so far i feel like i'm working without a net
[2024/06/26 11:51]  Dizzi Sternberg: we will draw that soon :)
[2024/06/26 11:51]  NightShade Fugu: Yes Janet
[2024/06/26 11:51]  NightShade Fugu: Sorry for the  complexity
[2024/06/26 11:52]  NightShade Fugu: But we arr all there
[2024/06/26 11:52]  NightShade Fugu: Have a bump  node
[2024/06/26 11:52]  NightShade Fugu: with an associated image
[2024/06/26 11:52]  Janet Rossini: somewhere
[2024/06/26 11:52]  NightShade Fugu: and changing  gray  tones in that
[2024/06/26 11:52]  NightShade Fugu: chould change the  normal map
[2024/06/26 11:53]  NightShade Fugu: add or  subtract from it
[2024/06/26 11:53]  Dizzi Sternberg: so this is useful for rivets?
[2024/06/26 11:53]  NightShade Fugu: Yes it is  usefull for  anything
[2024/06/26 11:54]  NightShade Fugu: I  will come to all the  options
[2024/06/26 11:54]  Janet Rossini: ok
[2024/06/26 11:54]  Dizzi Sternberg: embossing in metal
[2024/06/26 11:54]  Janet Rossini: i have the bump defined and linked
[2024/06/26 11:54]  NightShade Fugu: but  here the  important  thign is  the  way to add  the  bumpmap
[2024/06/26 11:54]  Janet Rossini: but no image yet
[2024/06/26 11:54]  Dizzi Sternberg: same here
[2024/06/26 11:54]  NightShade Fugu: You shoudl  have a  back image in the  Image display called  "bump" maybe
[2024/06/26 11:54]  NightShade Fugu: if you go to the  side  panel
[2024/06/26 11:54]  NightShade Fugu: with is the  image display
[2024/06/26 11:55]  Dizzi Sternberg: yes
[2024/06/26 11:55]  NightShade Fugu: you shoudl have a pictuure with the name you gave
[2024/06/26 11:55]  NightShade Fugu: and it  si  by default  black
[2024/06/26 11:55]  Dizzi Sternberg: yes
[2024/06/26 11:55]  Janet Rossini: i see an 8x8 square with no name
[2024/06/26 11:55]  Dizzi Sternberg: https://gyazo.com/6be978f905d143ea097915e692d5c44d
[2024/06/26 11:55]  NightShade Fugu: ok Janet
[2024/06/26 11:56]  Dizzi Sternberg: i had to find it in the dropdown
[2024/06/26 11:56]  NightShade Fugu: yes one need to  find it  in dropdown
[2024/06/26 11:56]  Janet Rossini: ok that was the secret step
[2024/06/26 11:56]  Janet Rossini: now i have a black thing, very large
[2024/06/26 11:56]  Dizzi Sternberg: :)
[2024/06/26 11:56]  Dizzi Sternberg: yes
[2024/06/26 11:56]  NightShade Fugu: always  hidden layers in blender
[2024/06/26 11:56]  NightShade Fugu: Smiels
[2024/06/26 11:57]  NightShade Fugu: sow e are pretty  well off
[2024/06/26 11:57]  NightShade Fugu: to make the  first  bump map changes
[2024/06/26 11:57]  NightShade Fugu: No  we have an image
[2024/06/26 11:57]  NightShade Fugu: and we like to change that
[2024/06/26 11:57]  NightShade Fugu: in order to do that
[2024/06/26 11:57]  Janet Rossini: ok black square
[2024/06/26 11:58]  NightShade Fugu: we need to  go to a new setup
[2024/06/26 11:58]  NightShade Fugu: Called Image paint
[2024/06/26 11:58]  NightShade Fugu: sorry texture Paint
[2024/06/26 11:58]  NightShade Fugu: "TEXTURE APAINT
[2024/06/26 11:58]  NightShade Fugu: Before ve do
[2024/06/26 11:58]  Dizzi Sternberg: ok
[2024/06/26 11:58]  NightShade Fugu: it is  cruciial  that we have selected the  image  we like  to change
[2024/06/26 11:58]  Dizzi Sternberg: ok
[2024/06/26 11:58]  Janet Rossini: jump from plane.
[2024/06/26 11:59]  Dizzi Sternberg: :)
[2024/06/26 11:59]  Janet Rossini: before jumping from plan, be sure you are wearing your chute.
[2024/06/26 11:59]  NightShade Fugu: So you have to click  in the  node tree
[2024/06/26 11:59]  NightShade Fugu: on the bump map  image
[2024/06/26 11:59]  NightShade Fugu: so it  get a  highlighted border
[2024/06/26 11:59]  Dizzi Sternberg: ok
[2024/06/26 11:59]  NightShade Fugu: then when you go  to  texture paint
[2024/06/26 11:59]  NightShade Fugu: that is the  image  you  work on
[2024/06/26 11:59]  Dizzi Sternberg: ok
[2024/06/26 12:00]  Janet Rossini: ok
[2024/06/26 12:00]  Janet Rossini: seems right. says bump. i see  black ckube
[2024/06/26 12:00]  NightShade Fugu: Ok  so my  window looks like this
[2024/06/26 12:00]  Dizzi Sternberg: https://gyazo.com/1c7164898987625c5b61f5d4925346a6
[2024/06/26 12:00]  Janet Rossini: yes
[2024/06/26 12:00]  NightShade Fugu: https://gyazo.com/09c7349b5b4a04e7a500dfa3f84bc712
[2024/06/26 12:00]  Dizzi Sternberg: ok
[2024/06/26 12:00]  NightShade Fugu: we have a image  display
[2024/06/26 12:01]  NightShade Fugu: and we have the  cube
[2024/06/26 12:01]  NightShade Fugu: one can change the  way  ti is  shown
[2024/06/26 12:01]  NightShade Fugu: using the  icon inthe  upper  right  corner
[2024/06/26 12:01]  NightShade Fugu: as in the  model  window
[2024/06/26 12:02]  NightShade Fugu: show  ti as a  mesh  or  with  fidderent  textures
[2024/06/26 12:02]  NightShade Fugu: the  best here is  to show  in  full render
[2024/06/26 12:02]  NightShade Fugu: https://gyazo.com/ab227bbe8d7e7a08b1767fbe528c998a
[2024/06/26 12:03]  Dizzi Sternberg: oki i hade to open the veiwport wide to see that
[2024/06/26 12:03]  NightShade Fugu: yes
[2024/06/26 12:03]  NightShade Fugu: some miht  be  hidden
[2024/06/26 12:03]  NightShade Fugu: So now  we  are in a  texture draw mode
[2024/06/26 12:03]  Janet Rossini: yes that is odd
[2024/06/26 12:03]  Janet Rossini: ok yes
[2024/06/26 12:03]  Dizzi Sternberg: yes
[2024/06/26 12:03]  Dizzi Sternberg: 2
[2024/06/26 12:03]  NightShade Fugu: and in the  texture panel
[2024/06/26 12:04]  NightShade Fugu: one can draw
[2024/06/26 12:04]  NightShade Fugu: as example  some  white line
[2024/06/26 12:04]  Dizzi Sternberg: (moves blender to Huion screen)
[2024/06/26 12:05]  Janet Rossini: what brush should we use?
[2024/06/26 12:05]  NightShade Fugu: So if one pla  with the  Display
[2024/06/26 12:05]  NightShade Fugu: on can switch
[2024/06/26 12:05]  NightShade Fugu: between different modes
[2024/06/26 12:05]  Janet Rossini: i just have the one i guess texdraw
[2024/06/26 12:05]  NightShade Fugu: Se ejust the  texture
[2024/06/26 12:06]  NightShade Fugu: or the  full render
[2024/06/26 12:06]  Janet Rossini: ?
[2024/06/26 12:06]  Dizzi Sternberg: https://gyazo.com/9306dad08d43a09189b9b7b8f22cbcbc hehe
[2024/06/26 12:06]  NightShade Fugu: https://gyazo.com/b85953c3d8c28897d29735024d242342
[2024/06/26 12:06]  NightShade Fugu: my  thing  in texture mode
[2024/06/26 12:07]  NightShade Fugu: and we can see the  UV is  repeated many  times
[2024/06/26 12:07]  Dizzi Sternberg: the brush size is [ and ]
[2024/06/26 12:07]  Dizzi Sternberg: like in PS
[2024/06/26 12:07]  Dizzi Sternberg: and CSP
[2024/06/26 12:08]  NightShade Fugu: yes
[2024/06/26 12:08]  Janet Rossini: mine is not changing the picture
[2024/06/26 12:09]  Janet Rossini: https://gyazo.com/05f3868b2e33842f347e1a7a4d3627a9
[2024/06/26 12:09]  NightShade Fugu: Janet
[2024/06/26 12:09]  NightShade Fugu: I  think i  made amistake
[2024/06/26 12:09]  NightShade Fugu: mistake
[2024/06/26 12:09]  NightShade Fugu: int he  node tree
[2024/06/26 12:09]  Janet Rossini: ok
[2024/06/26 12:10]  NightShade Fugu: https://gyazo.com/1b73c7a78872a9db6e594c09dd312b2b
[2024/06/26 12:10]  NightShade Fugu: the  bump map  picture has to be  inputted to the  hight
[2024/06/26 12:10]  NightShade Fugu: like shown here
[2024/06/26 12:10]  NightShade Fugu: Sorry  (mistakes happens)
[2024/06/26 12:11]  NightShade Fugu: int he  end
[2024/06/26 12:11]  Janet Rossini: ah yes much better
[2024/06/26 12:11]  Janet Rossini: :)
[2024/06/26 12:11]  NightShade Fugu: we shoudl see somethign liek this
[2024/06/26 12:11]  Dizzi Sternberg: i made a mistake and connected it
[2024/06/26 12:11]  NightShade Fugu: good  Dizzi
[2024/06/26 12:11]  NightShade Fugu: Also make more sence
[2024/06/26 12:11]  NightShade Fugu: sense
[2024/06/26 12:11]  NightShade Fugu: so we see anythign we draw
[2024/06/26 12:11]  NightShade Fugu: on the  picture is  nor refleced in a change fo the  normal  map
[2024/06/26 12:12]  NightShade Fugu: So
[2024/06/26 12:12]  NightShade Fugu: Now we need to knwo  abit of how th e bump map  are jandeled
[2024/06/26 12:12]  NightShade Fugu: handeled
[2024/06/26 12:13]  NightShade Fugu: gray  128   is no change
[2024/06/26 12:13]  NightShade Fugu: and more white  is  up
[2024/06/26 12:13]  NightShade Fugu: darker is  down
[2024/06/26 12:13]  NightShade Fugu: So the  normal  way to do  a bump map
[2024/06/26 12:13]  NightShade Fugu: is  to make  it  uniform gray
[2024/06/26 12:13]  NightShade Fugu: and the add hight or  dept
[2024/06/26 12:14]  NightShade Fugu: so  just colour pick a  mid  gray tome  and
[2024/06/26 12:14]  Dizzi Sternberg: so set grey and a big brush and paint it all?
[2024/06/26 12:14]  NightShade Fugu: then paint the picture with a  huge  brush
[2024/06/26 12:14]  NightShade Fugu: make it all gray
[2024/06/26 12:14]  Janet Rossini: i have a question
[2024/06/26 12:14]  NightShade Fugu: yes
[2024/06/26 12:14]  NightShade Fugu: Yes Janet ?
[2024/06/26 12:14]  Janet Rossini: i was drawing in white, as i think you were, and got the pattern on the cube as you had (I think)
[2024/06/26 12:15]  NightShade Fugu: yes
[2024/06/26 12:15]  Janet Rossini: then i tried to erase it and painted all in black ...
[2024/06/26 12:15]  NightShade Fugu: yes
[2024/06/26 12:15]  Janet Rossini: and the pattern does not go away even tho the texture looks black
[2024/06/26 12:15]  NightShade Fugu: and it  vanished
[2024/06/26 12:15]  Dizzi Sternberg: IT SEEMS TO PAINT IN MULTIPLY
[2024/06/26 12:15]  Dizzi Sternberg: sorry
[2024/06/26 12:16]  Dizzi Sternberg: i had to go over several times
[2024/06/26 12:16]  Janet Rossini: ah blending mode
[2024/06/26 12:17]  Dizzi Sternberg: had to go over 10 times
[2024/06/26 12:17]  NightShade Fugu: it is  like photoshop
[2024/06/26 12:17]  NightShade Fugu: with  diferent  way  to  mic  brushes
[2024/06/26 12:17]  Dizzi Sternberg: yes it was in mix
[2024/06/26 12:17]  NightShade Fugu: mix
[2024/06/26 12:17]  Dizzi Sternberg: yes i understand that
[2024/06/26 12:18]  NightShade Fugu: I think the  main thign here
[2024/06/26 12:18]  Janet Rossini: nothing i do seems to make it go away
[2024/06/26 12:18]  NightShade Fugu: is one can get to the  texture paint
[2024/06/26 12:18]  NightShade Fugu: and get the  right  texture selected
[2024/06/26 12:18]  NightShade Fugu: and actually see how  one  cange the  bumpmap
[2024/06/26 12:19]  NightShade Fugu: But we are not  done
[2024/06/26 12:19]  NightShade Fugu: ecause  we have  even more poverfull tools  here
[2024/06/26 12:19]  NightShade Fugu: One can draw ont he  cube  directly  too
[2024/06/26 12:19]  NightShade Fugu: and it  wil change the  image  selected nothing  else
[2024/06/26 12:20]  NightShade Fugu: So if we all make the  image  grayish
[2024/06/26 12:20]  Janet Rossini: nothing i do affects the cube
[2024/06/26 12:20]  NightShade Fugu: Ok Janet
[2024/06/26 12:20]  NightShade Fugu: So did  you  fix the little thing with the  node tree
[2024/06/26 12:21]  NightShade Fugu: https://gyazo.com/c92f59f240db9c339ddec326b5bc9723
[2024/06/26 12:21]  Janet Rossini: yes and i have the crosshatch but that is now all i can get even if i paint more
[2024/06/26 12:21]  NightShade Fugu: colout input  from the texture  has to go into the hght
[2024/06/26 12:22]  Janet Rossini: https://gyazo.com/e054eb0c4817d6488e412e3865653f6a
[2024/06/26 12:22]  NightShade Fugu: Ok  so go back to the node tree
[2024/06/26 12:22]  NightShade Fugu: ok that might  be  ok  Janet
[2024/06/26 12:22]  NightShade Fugu: try to  make a  unifor colour in grqay  all over the  image
[2024/06/26 12:22]  Janet Rossini: https://gyazo.com/1004573d08c659ad65c176c5177662dc
[2024/06/26 12:23]  NightShade Fugu: nodes are fine
[2024/06/26 12:24]  NightShade Fugu: so  if w e get the  image  in a  gray  tone  unifor all hight  changes shoudl vanish
[2024/06/26 12:25]  Janet Rossini: now it did this https://gyazo.com/3240d485f72c66a976dbe0fc9e7baff5
[2024/06/26 12:25]  NightShade Fugu: smiles
[2024/06/26 12:25]  NightShade Fugu: are yo sure you  ahve the  right  image  selected
[2024/06/26 12:25]  NightShade Fugu: int he texture paint
[2024/06/26 12:26]  NightShade Fugu: there si  somethign  makign bumps
[2024/06/26 12:27]  Dizzi Sternberg: try going over the area a few times
[2024/06/26 12:27]  Dizzi Sternberg: it took 10 passes for me to flatten it
[2024/06/26 12:28]  NightShade Fugu: set the  strength  to 100
[2024/06/26 12:28]  NightShade Fugu: of the  brush
[2024/06/26 12:28]  Dizzi Sternberg: and i could not see the lines in the texture
[2024/06/26 12:30]  Janet Rossini: max strength is 10
[2024/06/26 12:30]  Dizzi Sternberg: maybe why i had to pass over 10 times
[2024/06/26 12:31]  NightShade Fugu: For now  no not  change the  node settings  janet
[2024/06/26 12:31]  Janet Rossini: i am not changing any node settings
[2024/06/26 12:31]  NightShade Fugu: can you  give us a  picture fo the  full screen
[2024/06/26 12:31]  Dizzi Sternberg: its the brush
[2024/06/26 12:31]  NightShade Fugu: so we can see the  selections meny bars
[2024/06/26 12:32]  Janet Rossini: https://gyazo.com/a47c1752ba578e8c2b7710d25c3e3504
[2024/06/26 12:33]  Dizzi Sternberg: set the radius large and scrubb the area a lot
[2024/06/26 12:33]  Dizzi Sternberg: down to grey
[2024/06/26 12:33]  Dizzi Sternberg: and watch the stuff in the 3d window
[2024/06/26 12:33]  Dizzi Sternberg: see it the scratches get less
[2024/06/26 12:34]  NightShade Fugu: An other  thing might  to try to save the  bump  image
[2024/06/26 12:34]  Dizzi Sternberg: i had to scrub the window 10 times before the brush cleaned the previos
[2024/06/26 12:34]  Janet Rossini: i have been scrubbing and scrubbing
[2024/06/26 12:34]  Dizzi Sternberg: ok
[2024/06/26 12:36]  NightShade Fugu: Try  to save the  Bump immage
[2024/06/26 12:36]  NightShade Fugu: to the  drive
[2024/06/26 12:36]  Janet Rossini: how does one do that
[2024/06/26 12:36]  NightShade Fugu: Sometimes bender do not  update  if there is not  file to save to
[2024/06/26 12:36]  NightShade Fugu: Click in the minu  on image
[2024/06/26 12:36]  NightShade Fugu: and save
[2024/06/26 12:37]  NightShade Fugu: or save as
[2024/06/26 12:37]  Janet Rossini: k done
[2024/06/26 12:37]  Janet Rossini: that cleared it
[2024/06/26 12:37]  Janet Rossini: sheesh
[2024/06/26 12:37]  NightShade Fugu: yes
[2024/06/26 12:37]  NightShade Fugu: sorry  ti is a  old Blender  problem
[2024/06/26 12:38]  Janet Rossini: sorry for the delay.
[2024/06/26 12:38]  Dizzi Sternberg: np
[2024/06/26 12:38]  NightShade Fugu: took me  tons of  frustration
[2024/06/26 12:38]  Dizzi Sternberg: explains why it happened here too
[2024/06/26 12:38]  NightShade Fugu: and headace to find what i  lost
[2024/06/26 12:38]  NightShade Fugu: But we gt a  logn  way
[2024/06/26 12:39]  NightShade Fugu: we have a  texture with  can be a bump map
[2024/06/26 12:39]  NightShade Fugu: and can paint on that
[2024/06/26 12:39]  NightShade Fugu: Next
[2024/06/26 12:39]  Dizzi Sternberg: https://gyazo.com/dd897a348a539b87bd6444bc042af944
[2024/06/26 12:39]  NightShade Fugu: Now we have  cleared the  bump map
[2024/06/26 12:39]  NightShade Fugu: we can go the  the  image  display  window
[2024/06/26 12:39]  NightShade Fugu: and then draw dirctly on the  cube
[2024/06/26 12:39]  Dizzi Sternberg: yes
[2024/06/26 12:39]  NightShade Fugu: wotks  the  same  waqy
[2024/06/26 12:40]  NightShade Fugu: way
[2024/06/26 12:40]  Dizzi Sternberg: :)
[2024/06/26 12:40]  NightShade Fugu: and one can add doth and critical thign to the  3d model
[2024/06/26 12:40]  Janet Rossini: bah
[2024/06/26 12:40]  Janet Rossini: now it is stuck flat
[2024/06/26 12:41]  NightShade Fugu: yes
[2024/06/26 12:41]  NightShade Fugu: so you  got all flat again  janet
[2024/06/26 12:41]  NightShade Fugu: then try to  so to the  model  window
[2024/06/26 12:41]  NightShade Fugu: and use the  brudh there
[2024/06/26 12:41]  Janet Rossini: and nothing i draw in the square or on the cube makes any difference
[2024/06/26 12:42]  Janet Rossini: whether i draw in black or white
[2024/06/26 12:42]  NightShade Fugu: mmmmmmmmmmm
[2024/06/26 12:42]  Dizzi Sternberg: what colour pen?
[2024/06/26 12:42]  Dizzi Sternberg: ok
[2024/06/26 12:43]  NightShade Fugu: ok that is  odd
[2024/06/26 12:43]  Janet Rossini: ok i saved the file andn reopened ad now:
[2024/06/26 12:44]  Dizzi Sternberg: and worked?
[2024/06/26 12:44]  NightShade Fugu: Ok
[2024/06/26 12:44]  NightShade Fugu: it  shoudl be  dynamic
[2024/06/26 12:44]  Janet Rossini: oh wait not in cycles
[2024/06/26 12:44]  Dizzi Sternberg: im in evee
[2024/06/26 12:44]  NightShade Fugu: ok that  may  explain
[2024/06/26 12:45]  Janet Rossini: fuck me. which are we supposed to be in?
[2024/06/26 12:45]  Dizzi Sternberg: cycles i think
[2024/06/26 12:45]  Dizzi Sternberg: i forgot
[2024/06/26 12:45]  NightShade Fugu: yes try  cucles
[2024/06/26 12:45]  NightShade Fugu: Eevee shoudl show  bump map  too though
[2024/06/26 12:45]  Janet Rossini: now i have this: https://gyazo.com/3487b0685bab56e84d361211c29a3cbb
[2024/06/26 12:45]  Dizzi Sternberg: it did
[2024/06/26 12:46]  NightShade Fugu: ok that is  fine  Janet
[2024/06/26 12:46]  NightShade Fugu: then you have to select a better display
[2024/06/26 12:46]  NightShade Fugu: it is  the  icons in the  upper corner
[2024/06/26 12:46]  Janet Rossini: yes it lost that setting
[2024/06/26 12:46]  NightShade Fugu: whare you select  between  mesh  faces texture or  full render
[2024/06/26 12:47]  Dizzi Sternberg: yes was like this https://gyazo.com/b81a36d7ff89cf415f9bcde208a3087c
[2024/06/26 12:47]  NightShade Fugu: https://gyazo.com/a0623dc2b7b45cff17c0669b6da0aea0
[2024/06/26 12:47]  NightShade Fugu: you can  swith  to see  the  textur  onthe  onject or the  render of all
[2024/06/26 12:48]  NightShade Fugu: you see the  texture directly
[2024/06/26 12:48]  Eye of Odin HUD to wear: + LibbyCoker  [4]
[2024/06/26 12:49]  Eye of Odin HUD to wear: - LibbyCoker  [3]
[2024/06/26 12:49]  NightShade Fugu: Actually i think it  works best in eeevee
[2024/06/26 12:49]  NightShade Fugu: EEVEE
[2024/06/26 12:50]  Dizzi Sternberg: yes its less grainy
[2024/06/26 12:50]  NightShade Fugu: yes and  faster update of the  bump
[2024/06/26 12:51]  NightShade Fugu: But we need to get Janet in line
[2024/06/26 12:51]  Janet Rossini: again i cannot draw
[2024/06/26 12:51]  NightShade Fugu: Ok Save the  file
[2024/06/26 12:51]  NightShade Fugu: close the  all
[2024/06/26 12:51]  NightShade Fugu: then reopen
[2024/06/26 12:51]  NightShade Fugu: you  shoudl get back to  whare you are
[2024/06/26 12:52]  Dizzi Sternberg: yes but you could draw this externally in Procreate or PS
[2024/06/26 12:52]  Janet Rossini: i yes but still cannot draw on the image or cube
[2024/06/26 12:52]  Dizzi Sternberg: ok
[2024/06/26 12:52]  Dizzi Sternberg: i see
[2024/06/26 12:52]  NightShade Fugu: So try  to close it  Janet
[2024/06/26 12:52]  NightShade Fugu: somethign got  stuck
[2024/06/26 12:53]  Janet Rossini: closed and reopened blender still nothing
[2024/06/26 12:53]  NightShade Fugu: then reopen the  blender file
[2024/06/26 12:53]  NightShade Fugu: whispers: and you can not  draw ont he  image ????
[2024/06/26 12:54]  Janet Rossini: i can draw in white on gray but not black
[2024/06/26 12:54]  Dizzi Sternberg: these are my brush settings https://gyazo.com/3288e82a973b80f5751cda17136c53d2
[2024/06/26 12:54]  NightShade Fugu: Shoud draw  thing  white lines
[2024/06/26 12:54]  NightShade Fugu: thin
[2024/06/26 12:54]  NightShade Fugu: white lines
[2024/06/26 12:55]  Dizzi Sternberg: yes
[2024/06/26 12:55]  Dizzi Sternberg: it does
[2024/06/26 12:55]  Janet Rossini: it's sort of working now
[2024/06/26 12:55]  Janet Rossini: no idea what changed
[2024/06/26 12:55]  Dizzi Sternberg: yes?
[2024/06/26 12:55]  Janet Rossini: anyway i think i understand up to now what should be possible
[2024/06/26 12:55]  NightShade Fugu: Ok se we have  to align again
[2024/06/26 12:55]  NightShade Fugu: we all make the  immage  a gray tone
[2024/06/26 12:56]  NightShade Fugu: and bump  should  vanish
[2024/06/26 12:57]  NightShade Fugu: then we can  go to the  model  window
[2024/06/26 12:57]  NightShade Fugu: and try t make  bump  by  direct draw ont he  cube
[2024/06/26 12:57]  NightShade Fugu: make some dots around
[2024/06/26 12:58]  NightShade Fugu: somethign liek this
[2024/06/26 12:58]  NightShade Fugu: https://gyazo.com/fd060fd2497d4e12ab40b86b4a3dc1ce
[2024/06/26 12:59]  NightShade Fugu: it shoudl change the  image
[2024/06/26 12:59]  NightShade Fugu: relecting the  change
[2024/06/26 12:59]  NightShade Fugu: reflecting the  changes
[2024/06/26 12:59]  NightShade Fugu: You got that ?
[2024/06/26 13:00]  Janet Rossini: shouts: yes i managed to get something like rivets. but you have to paint a lot to get it flat again. perhaps best to start with new textures
[2024/06/26 13:00]  Janet Rossini: sorry
[2024/06/26 13:00]  NightShade Fugu: Smiles
[2024/06/26 13:00]  NightShade Fugu: Ok Janet
[2024/06/26 13:00]  NightShade Fugu: as long we have  some  dots
[2024/06/26 13:00]  Dizzi Sternberg: yes im seing same sort of stuff, why not make a texture in 128 grey and load it before scrawling on it
[2024/06/26 13:01]  NightShade Fugu: one can  do that
[2024/06/26 13:01]  NightShade Fugu: it  takes me 2 strokes to go gray
[2024/06/26 13:01]  NightShade Fugu: make a brush 1000 pt
[2024/06/26 13:01]  Dizzi Sternberg: ok
[2024/06/26 13:01]  NightShade Fugu: and then 1000 percent
[2024/06/26 13:01]  Dizzi Sternberg: https://gyazo.com/781583771e447083de4382c492d630ba
[2024/06/26 13:01]  NightShade Fugu: and it  delete all
[2024/06/26 13:02]  Dizzi Sternberg: where is the 1000% ?
[2024/06/26 13:02]  NightShade Fugu: Sorry strength 10000
[2024/06/26 13:02]  NightShade Fugu: 1.0000
[2024/06/26 13:02]  Dizzi Sternberg: ok
[2024/06/26 13:02]  NightShade Fugu: full strength and mix
[2024/06/26 13:02]  NightShade Fugu: overwrite what is there
[2024/06/26 13:02]  Dizzi Sternberg: yes
[2024/06/26 13:02]  NightShade Fugu: We all have  dots
[2024/06/26 13:03]  NightShade Fugu: Janet  you got  some
[2024/06/26 13:03]  Dizzi Sternberg: ill try wiping what i have clean then
[2024/06/26 13:03]  NightShade Fugu: Ok  Dizzi
[2024/06/26 13:03]  Janet Rossini: now i can draw in the texture and not on the cube. wtf.
[2024/06/26 13:04]  NightShade Fugu: then save texture  janet
[2024/06/26 13:04]  Dizzi Sternberg: wiped clean still bumpy
[2024/06/26 13:04]  Dizzi Sternberg: https://gyazo.com/98e7368eaacefb95de466d99d0f6c73f
[2024/06/26 13:04]  NightShade Fugu: yes it is nto  clean Dizzi
[2024/06/26 13:04]  NightShade Fugu: But before we all get totally  frustrated
[2024/06/26 13:04]  Dizzi Sternberg: took 5 passes
[2024/06/26 13:04]  Dizzi Sternberg: yes
[2024/06/26 13:04]  NightShade Fugu: Please make some  dots of some kind
[2024/06/26 13:05]  Dizzi Sternberg: ok
[2024/06/26 13:05]  NightShade Fugu: and tell me if  you have
[2024/06/26 13:05]  Dizzi Sternberg: https://gyazo.com/446c2dc5c49530aba534260ebd043671
[2024/06/26 13:06]  NightShade Fugu: good  Dizzi
[2024/06/26 13:06]  Janet Rossini: https://gyazo.com/0fb02ef4cd832b2693d9e754b57dde45
[2024/06/26 13:06]  NightShade Fugu: good Janet
[2024/06/26 13:06]  NightShade Fugu: Ok
[2024/06/26 13:06]  Dizzi Sternberg: :)
[2024/06/26 13:06]  NightShade Fugu: The strength of the bumpmap
[2024/06/26 13:06]  Janet Rossini: i think i get the idea but i have no clue why it works sometimes and not others
[2024/06/26 13:06]  NightShade Fugu: the  power  how  ti is  displayed
[2024/06/26 13:06]  NightShade Fugu: is determined int he node tree
[2024/06/26 13:07]  NightShade Fugu: and that si  important to know that once can change the  strength
[2024/06/26 13:07]  NightShade Fugu: we  run  on  a  huge amplification
[2024/06/26 13:07]  NightShade Fugu: so we  go back to the shader editir
[2024/06/26 13:07]  NightShade Fugu: editor
[2024/06/26 13:07]  NightShade Fugu: find the bump  node
[2024/06/26 13:07]  NightShade Fugu: and notice there is a  strength setting
[2024/06/26 13:08]  NightShade Fugu: it is  by default set to  1.000
[2024/06/26 13:08]  Dizzi Sternberg: yes
[2024/06/26 13:08]  NightShade Fugu: not try to change  to  0.1
[2024/06/26 13:08]  NightShade Fugu: reduce by  10  times the  strength
[2024/06/26 13:08]  Janet Rossini: ah it is range 0-1
[2024/06/26 13:09]  Dizzi Sternberg: https://gyazo.com/e28ccef593bd1afb5cdd1d22e533510d
[2024/06/26 13:09]  NightShade Fugu: yes and one can tyne the effect of the   bumpmap
[2024/06/26 13:09]  NightShade Fugu: sliding it  up and  down
[2024/06/26 13:10]  NightShade Fugu: one can also play  with the  distance
[2024/06/26 13:10]  NightShade Fugu: it is  usuallt  set to 1 and keept  fixed
[2024/06/26 13:10]  Dizzi Sternberg: what does it do?
[2024/06/26 13:10]  NightShade Fugu: usually
[2024/06/26 13:10]  NightShade Fugu: it compress the  information in the  bumpmap  picture
[2024/06/26 13:10]  NightShade Fugu: if the strength is  1
[2024/06/26 13:10]  Dizzi Sternberg: ok
[2024/06/26 13:11]  NightShade Fugu: light gray  is already out of  range
[2024/06/26 13:11]  NightShade Fugu: and  Black is  out of  range
[2024/06/26 13:11]  NightShade Fugu: so you get  jetky  bumpmaps
[2024/06/26 13:11]  NightShade Fugu: with flat tops and growes
[2024/06/26 13:11]  Dizzi Sternberg: ok
[2024/06/26 13:11]  NightShade Fugu: So  one  have to  tune the bumpmap  into a proper range
[2024/06/26 13:12]  NightShade Fugu: It also means
[2024/06/26 13:12]  Dizzi Sternberg: so leave at 1?
[2024/06/26 13:12]  NightShade Fugu: one are more free to  draw the  bumpmap
[2024/06/26 13:12]  Janet Rossini: i suppose there is some way to create more than one and use them?
[2024/06/26 13:12]  NightShade Fugu: Strength  is about  0.1 - 0.3 maybe
[2024/06/26 13:12]  NightShade Fugu: Distance  keep  on  1
[2024/06/26 13:13]  Dizzi Sternberg: ok
[2024/06/26 13:13]  NightShade Fugu: Ok
[2024/06/26 13:13]  NightShade Fugu: so what we have  now
[2024/06/26 13:13]  NightShade Fugu: is some controll of  how a  bumpmap will affect the  model
[2024/06/26 13:13]  Janet Rossini: yes, and i crave a break :)
[2024/06/26 13:13]  Janet Rossini: but i think i mostly get the idea
[2024/06/26 13:13]  NightShade Fugu: Yes  ajnet  Lol
[2024/06/26 13:13]  Dizzi Sternberg: :)
[2024/06/26 13:14]  NightShade Fugu: Next will eb  makign an external bump map
[2024/06/26 13:14]  NightShade Fugu: will be  much the  same
[2024/06/26 13:14]  Dizzi Sternberg: so basically how do we get this into SL?
[2024/06/26 13:14]  NightShade Fugu: that  ahs  to be  baked
[2024/06/26 13:14]  NightShade Fugu: has
[2024/06/26 13:14]  Dizzi Sternberg: next lesson
[2024/06/26 13:14]  NightShade Fugu: One  bake the normal map
[2024/06/26 13:14]  Dizzi Sternberg: save what we have?
[2024/06/26 13:14]  Janet Rossini: i'm sorry, i must log and undertake the bins.