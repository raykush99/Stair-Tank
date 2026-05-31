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

**Day 8**
Today, I countinued working on the Stair Tank. I decided to switch from an esp32 to a raspberry pi 4 as the main processor so I can get more computing power for future additions to the project. I started by taking my electrical schematic from the previous model and replacing the esp32 with a raspberry pi. I then rewired everything to the same corresdoning pins on the pi, making sure which are gpio, pwm, and I2C pins. One thing I had to figure out is how to connect the speaker to the pi. I discovered that I could use the 3.5 mm audio jack on the pi, and by using an audio wire and cutting the ends, I can connect the wires to the amplifier on the speaker to make it work. In the end, I re-did the electrical schematic and got ready to modify the project based on a raspberry pi based infrastructure.
<img width="1551" height="1074" alt="image" src="https://github.com/user-attachments/assets/2369a6ef-1248-4e8b-9732-5f4cb6f97e78" />

**Day 9**
Today was a straight forward day. I cut the panels from ABS plastic sheets using a scroll saw. Because some of the panels had curved parts and geometery that would have been hard to mark on a sheet, to ensure that I cut everything to the correct dimensions, I printed a schematic of the panels using a 1:1 ration and taped them onto the platic pieces. This way I can cut all the pieces by following the lines on the printed paper.
<img width="1451" height="1125" alt="image" src="https://github.com/user-attachments/assets/6b54db34-3f49-4efe-ae80-2d0c3f6dc27b" />

**Day 10**
Today was connecting the speaker to the rasberry pi. I cut the audio wire from old headphones, but found that it had three wires. I realized that one was ground and one for left and right side audio each. I had one speaker, so I connected the right and left audio into one sound. When I tested it, it didn't work, so I used a multimeter to test continuity. I realized that the wires had a thin layer of insulation, on them. Since it was too thin to strip, I decided to put a layer of solder on the wire to create a conductive surface. The solder fused the two sounds into one wire, and also burned away the insulation to expose the copper underneath. I tested again, but realized the amplifier board needs extranl power. After giving it 12 volts extrnal power, I tested again. I also realized that the board had the ability to connect audio via bluetooth. So insteas of using the audio jack, I turned on the pi, and using a remotre VNC server, I connected the speaker to the pi via bluetooth and tested by playing music. I then set the bluetooth devide to auto connect when turned on so the speaker connects automatically.
<img width="389" height="244" alt="image" src="https://github.com/user-attachments/assets/fd9618fc-5fb6-401f-bd0a-2199f197c68e" />

**Day 11**
Today I started assembling the panels. I started with the side treads and side arms. I decided to use bamboo sticks as the axles for the idle axles, and lego exles for the active axles. I drilled the respective sized holes into every panel. For the lego axles, they only need to extrude from one side, so I didn't drill a hole on the other side to prevent the axle from falling out. To hold the axle in place, I glued a circlular piece to the other side that the axle can sit inside. Then, using the treads to measure, I cut cardbaord pieces to be put betwenn the panels to hold them together. I repeated all of this for the other arm and the side treads. I am using lego treads and wheels so I can easily customize the length, so I added the bamboo and lego axles and the wheel and hot glued them so they don't fall out. I also added small cardboard circles to the axles to prevent the wheels from sliding side to side and holding them in place.
<img width="448" height="273" alt="image" src="https://github.com/user-attachments/assets/d163d53b-76d6-4cfa-9d15-29202ba3f3b0" />

**Day 12**
After testing with a motor, I realized the treads were too loose and kept slipping off. Removing one piece made it too tight, so I decided to add a tensioner. I added an extra wheel the to top middle, tensioning the treads upward. I used bolts to hold the brackets that held the wheel up so they don't slide down and change the tensioning. After I added the extra wheels, I texted again by attaching a motor to the axles and it worked perfectly. Also added finishing touches and ensured stability to all the parts. Then, I decided to attach the electronics onto the bottom panel. I planned a layout on the panel to ensure all the pieces fit properly. The raspberry pi was put in the front, so there is easy access to the camera and usb ports. The gyro sensor was put in the middle, and the battery in the back. I made a case for the  battery using cardboard that the battery can slide into and the motor control is glued on top of that. To keep the gyro flat, I made a cardboard table that lifts the gryo uo so the wires can easy funnel from underneath and connect to the raspberry pi. I then wired everything up, soldering some wire connections together and using the connection terminal on the motor controller to connect the rest. I also added a switch to the tank, drilling a hole on the bottom to access it to turn it on and off. Again, I needed a cardboard table to lift the switch up so it doesn't drag on the floor.
<img width="1182" height="390" alt="image" src="https://github.com/user-attachments/assets/f5da854d-3d0b-43f1-9cf8-d8f56f96f7ff" />
<img width="994" height="319" alt="image" src="https://github.com/user-attachments/assets/deedb98b-ea24-4e44-ab3a-e4babaec07f7" />
<img width="1508" height="643" alt="image" src="https://github.com/user-attachments/assets/7ac6bca6-dc8c-4c5f-a132-0dc1539aeee4" />

**Day 13**
Final building day. I assembled the chassis by connecting the side panels to the bottom panel. I used spare ABS sheets to lift the bottom panel up and keep it flat while I glue the sides on to ensure the bottom does no drag on the floor. I then attached the back panel on to add for rigidity and mounted the speaker to the back panel facing forward. I then back right brackets using cardboard and attached them onto the sides to help hold the side onto the bottom panel in case the glue fails. After the chassis was mechanically sound (minus the top and front panel so I can still access the inside), I started adding the motors onto the axles, using boxes made from cardboard to hold the motor at the correct height and position. I then finished wiring all the jumper pins into the raspberry pi, including the ones to control the motors and for the gyro. I connect the power to the speaker and tested all connections to see that it works perfectly. Next up, programming it to move.
<img width="1125" height="466" alt="image" src="https://github.com/user-attachments/assets/f370ed7c-485b-4c2b-97bc-4d9f9cbec9eb" />
<img width="923" height="560" alt="image" src="https://github.com/user-attachments/assets/0e4c9841-33ee-4820-9e7b-7f0ee2f16124" />

**Coding Day 1**
I started coding the tank. I started by creating a new folder on the pi, and then made a code to enable and view the camera feed from the tank. I then started making functions that move the robot in specific directions. I figured out how to enable GPIO pins and set different ones one to move the motors to move the robot. When I tested, it didn't work and I realized I needed to add PWM control to enable to motor control. So I research how to do PWM on the pi, and added the PWM control to each of the functions. I tested and it managed to work. I then added a variable to the functions to adjust speed of the robot and tested, realizing the robot won't move if the motors run at a speed less than 50%.

**Coding Day 2**
Today, I started making the server to run the tank. I used flask to set up a server to be able to view the camera feed of the pi on my normal computer. After I figured that out, I wanted to add controller control. I realized I can use the flask server, connect an xbox controller to the computer and control the tank. I set up the code for the browser to recieve controller input and set it to the pi, and tested it to move the robot (using the functions I created before). I got the  controller to send one signal and start the robot, but then it stopped sending signals and I couldn't control the robot anymore. Next time, I have to make the data transfer more consistent.

**Coding Day 3**
Today, I figured out how to use data from other buttons on the controller to control things like servos. I also wrote the code to not only move the robot forward and back, but also turn it left and right. I got the data to send more consistently.

**Build again**
During testing, a motor came off, so I had to re attach that, reinforcing it by adding foam underneath to hold it in place. Next, I decided to attach the arms to the tank and added the servo mount tot he arm and bottom panel. I am waiting to attach the servo until I can set it to position zero.
<img width="822" height="484" alt="image" src="https://github.com/user-attachments/assets/c643e5ce-f282-4275-a05b-24d093d6b4fa" />

**Coding Day 4**
I started by learning how to move a servo using a pi without jitter. I decided to use the pigpio library and tested using the servo. After setting it to zero, attach it onto the tank chassis. However, the pigpio library requiers a pulse value 500-2500 to move the servo. I wrote a function in which I can input an angle and it converts it to the pulse value required to go to that angle and sets the servo to that angle.

**Coding Day 5**
While testing, the data transfer failed again, and I got it to work but it stopped the camera feed from showing. To fix this, I decided to move the camera feed to its own sub-process so it doesn't steal processing from the controller data transfer. I tested again and got the data to transfer consistently while still showing camera feed. fter that, I added all the button commands into the html code and used three buttons in the python code to set the servo to set angle values. I programmed the buttons to control the servo, and tested it to see it run. Finally, I decided to run the server program on startup, trying to use the crowtab method first, but that failed. Next I tried using a system document to run the terminal command to run the program. I tested it and it worked, and will test for consistently next time.

