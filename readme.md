# 20210415_tradShuffle

[github](https://github.com/lg3bass/20210415_tradShuffle)

Tags:

#maxmsp #maxmspjitter #madewithjitter #creativecoding #generativeart #generativevisuals #abletonlive #max4live #video #art #glsl #boogie-woogie

##mSocial Media:

[Twitter](https://twitter.com/lg3bass/status/1386153856619405313?s=20)

[Instagram](https://www.instagram.com/p/COEqXgwnmOa/?utm_source=ig_web_copy_link)


## Shader:

[Smoothstep.io](https://smoothstep.io/anim/a5d943cf9cc6)

## Description:

This project is a test of my ADSR device. (ADSR_0.249).  The animation was created in Ableton Live with Jitter Shader files.   The ADSR device is timeline to animate JXS shader files. 
 
The notable updates for this sprint are:

- ability to edit the function curves directly.
- ability to save out baked function curves to json.
- ability to create one-click ADSR keyframes.

## Workflow Notes:

The first thing is obviously recording and arranging the audio in Live.  I ususally start with some bass tracks but in this case I imported the audio and had to align it to a timeline.  I only took the first 12 bars and looped that.   Added some 7 string bass and found a nice canned percussion. 

the animation is done in 4 passes.   The first pass is to figure out what to animate. I found a great tool for composing shaders (smoothstep.io).   This is an online shader editor that has a timeline tool.  I have a boiler plate shader file I use to and modify this to make the shapes and layers used in my JXS file. 

The second pass I use my ADSR took to quickly set keyframes on a grid.  The idea behind this is to account for an anticipation ('A' of 'ADSR' attack state).  The ADSR tool will create a key with all 4 states at once so you do not have to key each one separately.  This allows for quick visualization and the ability to change easily.  I ususally loop a section of the arrangement view (2 bars) and 

The third pass is the Live automation pass.  Again I loop over 2 bars at a time and key the ADSR-automation_v0.05 params.  This sets the positions of the elements( e.g each circle,etc)

Finally I use bake the keyframes to function curves so I can fine tune the animation timing.  I did not need to spend a lot of time on this as the regular keying pass is usually sufficient. 

The best usage of the tool for now is to regularly disable draw on the UI menus. This competes with GLSL performance.  Another workflow is to click through the timeline in arrangement view.  Clicking redraws the screen and all automation.  You can work interactively this way see results real time. 

## Problems: 

M4L devices compete with GLSL performance.  If I hide the M4L devices I get 60fps.  If you want to record video make sure you hide the M4L GUI.  

Every time you make edits to the function curves directly you need to close the window to preview.  Again this competes with GLSL performance.  This is definitely a drag in my workflow I need to address. 

I need a way to delete whole sections of timeline ADSR keyframe data.  currently I have a draw selection tool but it would be better to have a marquee tool to select an entire box or maybe sections at a time. 

Save/Load ADSR json is still an issue.  This should be only one button to save all 4 tracks at a time. 

## Musical Performance: 

Also I am using this oppertunity to see how my bass playing style (4 fingerpicks) works with boogie woogie piano.  I do not know how to play boogie-woogie on the piano so I searched the internet for some boogie-woogie piano free midi files.  The result of that search was a piano player named Terry Butters in the UK. I like the result and will hit up a few piano players I know to maybe make some more examples.  I like the syncopation and there is a lot to explore here.

A big thank you to Terry for posting free midi examples.  He doesn't know I used a snippet.  To listen other music from Terry please visit:

### Terry Butters

[bandcamp](https://terrybutters.bandcamp.com/)

[free midi files](http://terrybutters.co.uk/terrybutters3.htm)