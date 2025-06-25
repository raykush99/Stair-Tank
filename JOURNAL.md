---
title: "Stair Tank"
author: "Kush Ray"
description: "A tank style RC car with camera that is able to go up and down stairs"
created_at: "2025-06-14"
---
**Total time spent: 15.5 desiging + 4.5 on github = 20 hours total**

**Day 1 June  13**       

Today I began my researching different methods of building a stair climbing robot. The main method I found was a modular robot in which each section could lift up one by one to climb stairs one at a time. I did not use this since I wanted to be able to place items on the top of my robot, and this would make that difficult. I wondered if there was a way the robot could directly go over the stairs, but that would require wheels bigger than 8 inches in raduis. I then had the idea of using tank treads. However, that would still need very long treads. Instead, I decided to make a way to expand the size of the treads, by including another set that can come out of the body of the robot. I used some spare LEGO pieces to make a quick prototype of the tread design, making sure it would work. After much trial and error, I found that including studs on the tracks helped it hold onto the stairs better. I also concluded that keeping a 45 degree angle was most effective in getting the treads to initially pull the robot up.    
![image](https://github.com/user-attachments/assets/894dda9d-bd02-4bb8-83fe-144a8931721f)             

**Time spent: 1.5 hours**

**Day 2 June 16**             
Today I began working on the CAD. I knew the tank had to be large to climb the stairs, so I decided to make it 18" x 12" x 12". I started making the panel that would hold the treads, and added fillets on the corners so the treads would be completly flush against the panel. I also added an extra hole in case the treads need to be tensioned. Next, I make a simple CAD of the wheel as well as making the axles. I did the same thing to make the panels for the expanding treads, and made panels to connect the two tread panels together to get a basic form of the tank. I assembled all the parts together to see how the second treads would flip out from the front. One hard part was making the curved panels since they had to be the right angle and radius to work. I managed to use the sketch of the tread panels as reference for the radius and angle to make the curves panels.            
![image](https://github.com/user-attachments/assets/36f6bd73-8636-438a-b25a-d29ca3d39184)
![image](https://github.com/user-attachments/assets/a206e337-7992-4b2d-9bed-e0235a2d2a1b)      
![image](https://github.com/user-attachments/assets/a9f3a53e-df7a-43a4-9faa-80a03df92c5a)      

**Time spent: 3 hours**

**Day 3 June 17**             
Today was mainly for finding the parts to build the tank. I decided to use lego treads, since they could be fit to any size, and I was able to add grip stubs on them to help climb the stairs. Doing some research, I also found that the L298N board was best for controlling the direction and speed of two motors. I also decied that a 35T motor would give the best torque and spped for the tank, and found a rechargable 12V battery to use. The last thing I thought of was how to flip the secondary treads. I decided on a servo motor since it would be best on keeping a 45 degree angle with the stairs. I also found strong servos to be able to lift the secondary treads.           
![image](https://github.com/user-attachments/assets/f86b057f-92ae-4f38-bc43-d99139783f57)
![image](https://github.com/user-attachments/assets/0e44c1c0-414d-4418-ab89-67da427c1782)               
**Time spent: 1 hour**

**Day 4 June 19**            
Today I edited my cad to change the size based on parts I found and to add more detail. I started by adding detail to the gears. Then, I had to make the axles and space between the tread panels bigger, since the LEGO treads I found were bigger than I expected. After making this change, I had to fix my assembly, since the editing of the size caused some elements to become offset and merge. I also had to edit some dimensions of the panels to adjust for the large tread size. Finally, I added the treads to my design. This was the hardest and most time consuming part, since the treads were an irrugular shape. I wasn't able to animate the treads, but I was able to make a static design to simulate where they would go. I also added revolve mates and gear relations on the axle and gears to show how they will all move together.              
![image](https://github.com/user-attachments/assets/ff4bdb19-f4bc-40a0-b86c-6fc99675db0e)
![image](https://github.com/user-attachments/assets/5ba62cbd-a306-49af-b9a0-f6ca8c1355c2)                                


**Time spent: 2.5 hours**

**Day 5 June 20**                
Today, I looked for the rest of the parts. Since I want a camera, I was planning on using the esp32-cam. However, this model does not have enough ports to be able to handle all the motors I need. After some searching, I found the esp32-S3-cam, a camera board with more gpio pins. I also spent some time seeing which gpio pins were usable and not taken up by the camera and other internal functions. Another problem I had was how to build the acutal tank. I though 3D printing, but the panels were too big. Instead, I decided to use polycarb or plastic. But since my design has curved parts, I eventually settled for ABS, since it is cheaper than polycarb, but also easier to bend into the curved shape I want. I spent time to plan out how I was going to cut each panel out, in order to have to buy the  least amount of material possible. I decided to use 1/8 inch for the main pieces, and 0.06 inch for the curved and smaller pieces.        
![image](https://github.com/user-attachments/assets/62c688f9-5820-416c-84fc-72411648f3c1)
![image](https://github.com/user-attachments/assets/a65f4227-239a-4c1a-bd23-ec5efb9d9ced)               
**Time spent: 1 hour**

**Day 5 June 20**               
My second work session on the 20th included me making the circuit diagram. I found a website that had many parts and allowed for an easy way to make visual diagrams. I started by importing in all the parts. I decided on not using a pcb, since most components were spread out and a pcb would be impractical. The cicurt included two servo motors, two dc motors, a motor driver, the esp32, the gyro sensor (to read the tilt of the tank on the stairs), a battery, a switch (to turn the power on and off), and a voltage stepdown. Halfway through wiring the power, I realized I didn't have a way to power the microcontroller. I wanted everything to have power using one battery, but the esp32 would fry with a 12V battery. I did research and found a voltage stepdown can convert the 12V to 5V. The model I found even had a usbc end to connect directly to the microcontroller to power it. Another problem was deciding which pins to use on the microcntroller. This is since some pins are connected to internal functions that may cause the pin not to work. I used the pin diagram given my the manufacturer and did research to identify which pins were safe. I was still short 2 pins, so decided to use the SD card pins since my project does not need an SD card. I then color coded the wires (red for power, black for GND, yellow for servos, random for motor control).             
![image](https://github.com/user-attachments/assets/db19ce81-5275-4bf9-ab6d-22fa1a068965)                
**Time spent: 2 hours**

**Day 6 June 23**           
Today, I decided to add my motors and batteries into the CAD. Originally, I tried to find models of the motors I could upload, but I wasn't able to find any. Instead, I decided to use the scematics given to make my own simple model of the servos, DC motors, and battery. After desgining each piece, I added it to the master assembly to see if it would fit. The DC motor and servo barely overlap with a few curved pieces, but this is fine since I can slightly change the curvature of the ABS while making it to fit the motors. I also added a simple mount for the servo to rest on and a piece to attach the servo shaft to the secondard tread piece. Finnally, I decided to customize the colors of each piece to what it would look like with the real materials, letting me finally finish the CAD for the stair tank.             
![image](https://github.com/user-attachments/assets/63faf58e-e27e-4e0e-ae77-bc1538ede891)
![image](https://github.com/user-attachments/assets/b6300b54-02c8-4fda-8237-e4a0409fa547)
![image](https://github.com/user-attachments/assets/0de8ce34-d16a-4db9-bc4f-6f852c96a8a7)       
**Time spent: 2 hours**         

**Day 7 June 25**
Today, I posted my design on pitstop and got some feedback. I decided to add mounts for the motors (however, thety are only half since the panels naturally support the other half of the motors). I also decided to shrink the height of the tank, from 6" to 4". This will make it cheaper to build and save space, giving it more structural integrity. Making this change was not too bad since I used con·straints previously, so most parts self corrected. Furthermore, I decided to add simple models of the rest of the electronics. I put the motor controller at the end by the motors. The esp32 is put on the front panel, since its camera has a very small cabel. This way the camera can extrude from the from plate. The voltage stepdown and gyro are also in the front, by the esp32. Also, I decided to add brackets to the inner sides as a way of connecting the tread plates to the bottom plate. This will make it easier to glue the two plates together. I also updates my BOM to reflect the decrease in size of the treads.       
![image](https://github.com/user-attachments/assets/c4ed86d2-6f73-4011-9462-65f93038884d)      
![image](https://github.com/user-attachments/assets/141f24bf-2504-44b9-89f1-d3379e6ea2bf)      
![image](https://github.com/user-attachments/assets/0f9dded5-d87e-447a-9375-68e8a4c40976)     
![image](https://github.com/user-attachments/assets/33946a73-2627-4625-bb07-3b0e0b4232f5)      
**Time spent: 2.5 hours**






