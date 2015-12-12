# Final-Project

## Project name: Eyeduino

### Summary: 

I am going to make an Arduino-powered head mounted display (HMD) unit akin to google glass, nicknamed "Eyeduino". I am hoping to use Eyeduino as a low-cost tool which can be utilized to prototype augmented reality projects, which is an area I am focusing on both in and outside of my classes at CCA. For this project, I am using the HMD for displaying a visual representation of data being collected by a sensor. To do this, I will be using an absolute orientation sensor to track Euler angles (pitch, roll, yaw), and the data generated will control a wireframe cube which is being displayed on a tiny OLED screen. The orientation sensor will be mounted onto the HMD and act as a way of head-tracking, thus altering the viewer’s perspective of the cube as they move their head. The device explores the concept of creating user interaction with 3D augmented information. Though it is simply a cube which is being displayed, this is a representation of how graphical user interfaces (GUI), something which has mainly remained in the two-dimensional realm, may be viewed through augmented/mixed reality displays. The information from the OLED will be reflected through a beam splitter lens crafted from laser-cut acrylic pieces, directly into the user’s eye. To create this, I have done a large amount of research on the technology used by Google Glass, Microsoft Hololens, and others, and figured that the most economical yet effective method is to replicate what is called a “Flat combiner 45 degrees”, which is what Google Glass uses. Other headsets use different iterations of waveguide display technology, and this is somewhat more challenging to replicate in a DIY fashion. If I am able to prototype this device successfully, then I will have the ability to create other versions with additional sensors and craft new methods of visualising sensor data. 

### Component Parts: 

BNO055 Absolute Orientation Sensor, OLED Display, 3V Pro Trinket, Adafruit Pro Trinket LiIon/LiPoly Backpack Add-On, Power Switch, Prism Lens, Shop Glasses


### Timeline:

 Week 1 (Nov. 11) - Assemble parts on breadboard, download and dissect libraries, figure out code structure. 
 
 Week 2 (Nov. 18) - Coding
 
 Week 3 (Nov. 25) - Coding and Hardware
 
 Week 4 (Dec. 2) - Hardware, design and 3D print enclosure if possible
 
 Week 5 (Dec. 9) - Present to class
 
 
 ### FINISHED PROJECT INFO (DEC. 10) 
 ## Summary:

The goal was to use Eyeduino as an exploration of HMDs and near-eye display technology, as well as to create a wearable device using an Arduino that has some relevance to augmented reality, which is an area I am hoping to design for in the near future. For this project, I am using the HMD in order to render a visual representation of data being collected by a sensor. To do this, I will be using an absolute orientation sensor to track Euler angles (pitch, roll, yaw), and the data generated will control a wireframe cube which is being displayed on a tiny OLED screen.

 The orientation sensor will be mounted onto the HMD and act as a way of head-tracking, thus altering the viewer’s perspective of the cube as they move their head. The device explores the concept of creating using head position to manipulate objects presented through an augmented reality wearable device. Though it is simply a cube which is being displayed, this is a representation of how graphical user interfaces (GUI), something which has mainly remained in the two-dimensional realm, may be viewed through augmented/mixed reality displays. The information from the OLED will be reflected through a beam splitter lens crafted from laser-cut acrylic pieces, directly into the user’s eye. 
To create this, I have done a large amount of research on the technology used by Google Glass and a few other devices, and figured that the most economical yet effective method is to replicate what is called a “Flat combiner 45 degrees”, which is what Google Glass uses. Other headsets use different iterations of waveguide display technology, and this is somewhat more challenging to replicate in a DIY fashion. This project is a first iteration of the concept, and I have the ability to create other versions with additional sensors and craft new methods of visualising sensor data. I am planning to construct a later version which uses a Rasberry Pi as opposed to a simple microcontroller, and probably explore a new method for creating the display.

Though having received a good amount of public backlash after its release, the Google Glass had some incredible engineering behind it, and it was my goal as a mere design student to replicate a more simple and cost-effective iteration. The device utilizes a LCoS screen (liquid crystal on silicon) as well as other light mechanics to project light through a series of beam splitters and then into the viewer’s line of sight.

 I was particularly fascinated by the prism mechanics of the combiner lense, so this was what I prototyped first using transparent acrylic pieces and a one-sided mirror piece which I laser-cut to exact measurements to fit over a small TFT display. 
 
My plan then was to create a miniature version of this setup and use a screen which would be brighter than the TFT, so I searched high and low and eventually found a little OLED screen that was only 60x32 pixels in size! Though I would have loved to have gotten my hands on an actual LCoS screen for this project, my hardware skills are still very beginner level and I can only imagine the issues I would run into when trying to hook one up to an Arduino. 

Next was to try and figure out the code. This took a while, as I had to go back and read up on the theory behind Euler angles and how I could use these principles when designing my cube animation. I also had to learn how to use the library for the tiny OLED display, which was quite cumbersome to code. Many headaches were had in this process, and though I inevitably succeeded in getting the code to function, there was still an issue of gimbal lock, i.e. when two out of the three axis are in the same plane, one degree of freedom is lost. My code contains a bitmap splashscreen of the CCA logo, followed by the cube animation which corresponds with the position of the absolute orientation sensor.


I then created a couple new beamsplitters to see which would fit the smaller screen better. 

I then created a couple new beamsplitters to see which would fit the smaller screen better. I tried to get the size and design of the beamsplitter lense as close to the real Google Glass as I could. 

 Having little to no experience in 3D modeling, I basically improvised a lot on this part of the project. I used Autodesk’s Fusion360 to model the enclosure for the electronics, and found it to be kind of beginner friendly. I chose to keep the wire bits still visible in order to give the piece a sort of cyberpunk aesthetic. 


Using some industrial strength velcro and a pair of shop glasses I took from CCA’s tech lab, as well as a sort of bro-y sunglasses retainer to house the battery, Eyeduino officially became a wearable device, enabling the viewer to gaze at a magical wireframe cube which they could view at different angles by simply moving their head. 





# Used Component Parts:
BNO055 Absolute Orientation Sensor, OLED Display, Arduino Nano, Prism Lens, Shop Glasses
Challenges:
Perhaps the biggest challenge is the code itself. I was learning how to use an obscure graphics library (u8glib), Adafruit unified sensor library, and the BNO055 specific library in order to make this work. What else was challenging was figuring out how to have the rotation matrix of the cube depend upon the X, Y, Z values (in degrees). This required a lot of float arrays, as well as translating the rotation matrix of Euler angles into code. 
 
 
