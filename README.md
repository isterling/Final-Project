# Final-Project

## Project name: Eyeduino

### Summary: 

I am going to make an Arduino-powered head mounted display (HMD) unit akin to google glass, nicknamed "Eyeduino". I am hoping to use Eyeduino as a low-cost tool which can be utilized to prototype augmented reality projects, which is an area I am focusing on both in and outside of my classes at CCA. For this project, I am using the HMD for displaying a visual representation of data being collected by a sensor. To do this, I will be using an absolute orientation sensor to track Euler angles (pitch, roll, yaw), and the data generated will control a wireframe cube which is being displayed on a tiny OLED screen. The orientation sensor will be mounted onto the HMD and act as a way of head-tracking, thus altering the viewer’s perspective of the cube as they move their head. The device explores the concept of creating user interaction with 3D augmented information. Though it is simply a cube which is being displayed, this is a representation of how graphical user interfaces (GUI), something which has mainly remained in the two-dimensional realm, may be viewed through augmented/mixed reality displays. The information from the OLED will be reflected through a beam splitter lens crafted from laser-cut acrylic pieces, directly into the user’s eye. To create this, I have done a large amount of research on the technology used by Google Glass, Microsoft Hololens, and others, and figured that the most economical yet effective method is to replicate what is called a “Flat combiner 45 degrees”, which is what Google Glass uses. Other headsets use different iterations of waveguide display technology, and this is somewhat more challenging to replicate in a DIY fashion. If I am able to prototype this device successfully, then I will have the ability to create other versions with additional sensors and craft new methods of visualising sensor data. 

### Component Parts: 

BNO055 Absolute Orientation Sensor, OLED Display, 3V Pro Trinket, Adafruit Pro Trinket LiIon/LiPoly Backpack Add-On, Power Switch, Prism Lens, Shop Glasses

### Challenges: 

Perhaps the biggest challenge is the code itself. I am basically learning how to use an obscure graphics library (u8glib), Adafruit unified sensor library, and the BNO055 specific library in order to make this work. What else is challenging is figuring out how to have the rotation matrix of the cube depend upon the X, Y, Z values (in degrees). This requires a lot of float arrays, as well as translating the rotation matrix of Euler angles into code. The hardware portion is not so difficult as I have already ordered, received, and soldered all my parts, as well as put together a Fritzing guide for wiring. 

### Timeline:

 Week 1 (Nov. 11) - Assemble parts on breadboard, download and dissect libraries, figure out code structure. 
 Week 2 (Nov. 18) - Coding
 Week 3 (Nov. 25) - Coding and Hardware
 Week 4 (Dec. 2) - Hardware, design and 3D print enclosure if possible
 Week 5 (Dec. 9) - Present to class
