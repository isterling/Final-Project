## Debug log

# Monday Nov. 16 

Received parts and tested everything with Arduino Nano. Everything was working as expected 
however ran into some hardware issues after rewiring. Tested BNO055 sensor with Nano and had issues with sensor
not being read on serial monitor. Attached it to a Uno and had no problems. I believe this to be a breadboard problem, 
however I must get another breadboard before continuing. I am running my OLED screen and BNO055 sensor off an Uno for now

Coding wise, I was able to sit and focus for two whole days and compile my code for the project. I was able to look at
some examples of using sensor data to be generated on an OLED, however the cube code was a bit trickier. I ran into some syntax
issues but Colin the lab monitor was able to help me out. These problems dealt with using a "do while" loop, I just 
forgot to put the "do" in my code. Everything is running smoothly so far, however I need to make some adjustments to the 
math once I have my finalized hardware components figured out for the head-mounted unit. I am sure I will be using this log
quite a bit for that portion. 

#Friday Nov. 20

Soldered parts together in an arrangement which would fit into a HMD(head-mounted display) type configuration. This was very difficult, as I had to resolder the ground and 3v3 wires several times to fit in an appropriate manner. This has almost been as frustrating as the code itself. Some girl also used almost all the heat shrink in the lab so I had to make do with whatever amount I could find. This has taken 6 hours. 

#Saturday Nov. 21

Played around with my code a bit to see if I could make my cube animation a bit slower. Ended up dividing the XYZ coordinate data by 50 and multiplying the Y coordinates by -1, I think this works well, not sure if reversing the Y coordinates really enhances it though. I am still trying to figure out why the cube is sort of jumpy in some areas. My educated guess is that the cube resets is because the coordinates experience gimbal lock. Gimbal lock is when two out of the three gimbals are in the same plane, one degree of freedom is lost. After doing a bit of research, I found out that this is a big problem is designing 3d modeling and games, so I am now understanding the pain that game developers face on a daily basis. After trying to fix this problem, I would get it to the point where the cube is stuck in a certain position, so I will leave it to where it just resets but is still interactive.

#Sunday Nov. 22

Created a few more prism lenses after working on the measurements to have it fit on the tiny OLED screen. This is a very time consuming process of laser cutting acrylic sheets sourced from TAP Plastics and then using ZAP glue to carefully put the pieces together. I have glued my fingers together twice, and it hurts. So far the prisms look good though

#Tuesday Nov. 24

Started the process of 3D Modeling a housing for the electronics in Fusion360. This is the first time I have used any 3D modeling software, so I am hoping that it will go smoothly. 

#Fri Nov. 27

After spending a while figuring out the 3D model, I made a design which I am happy with. I wanted to give it a sort of cyberpunk aesthetic and have the wires externally visible while the screen, arduino nano, and sensor are enclosed. I am currently 3D printing a rapid prototype to see how everything fits. This is also a first for me, as I do not really have much experience at all in 3D printing. 

#Sun. Nov. 29

Happy with how the components are fitting in the case, I am now going to print a final, high quality version of my model, estimated print time: 4.5 hours.

#Wed. Dec. 2

Everything is working well, I am figuring out how to mount the device on a pair of shop glasses sourced from the Hybrid Lab. You recommended I use industrial velcro, so I am going to pick that up this week 

#Fri. Dec. 4

Picked up some industrial strength velcro, works perfect. I have the battery pack for the device stored in some very bro-y sunglass retainers I found at REI. THANKFULLY the electronics are still intact and everything is working fine once I plug it in to the battery pack. I am not going to try and reconfigure anything out of fear that I will end up breaking it all. I have found that when worn, the cube does not experience the gimbal lock that frequently and doesn't really take away from the experience of having an augmented reality cube in front of your face. 
