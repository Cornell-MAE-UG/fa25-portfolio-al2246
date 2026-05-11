---
layout: project
title: Cube Craze Robot
description: MAE 3780 Robot Competition
technologies: [Arduino UNO, C++, Fusion 360]
image: /assets/images/robot.jpeg
---

## Introduction
For Cornell's mechatronics class we were tasked with designing a robot that would be able to drive on a board and collect more blocks than the opposing robot. 

## Robot Design and Strategy Overview
My team's robot design strategy was to keep it as simple as possible to limit the amount of issues that might arise. Our robot consists of the given chassis, a surrounding box enclosure with slots for our 3 QTI sensors, and a flap in the front. The flap ensures that the boxes can enter our robot perimeter, but cannot escape when continuing to drive or if we are getting pushed. We have used the small breadboard with the Arduino for wiring our motors and a larger breadboard for wiring our sensors. We used 3 QTI sensors located at the front left, front right, and center back of our robot. Ideally, during the competition our robot will start at an angle and head to the center right of the board then turn and move across the board in one initial pass to collect as many blocks as possible. Then our robot will continue to move forward and turn right or left depending on whether the left or right QTI sensor detects the black border. The robot will drice backwards when the back QTI sensor detects the border. When both the front QTI sensors detect the border the robot will stop. 


## Design Process Reflection
Our brainstorm plan worked well and for our front flap we came up with many possible ways to create it to make sure it would only open one way so blocks couldn’t escape. When we received the hinges we ordered they were quite stiff, so we used a thin piece of cardboard instead. The original wheels given were not providing great traction causing the timing for our turns to be off. To fix this temporarily we added rubber bands to the wheels. Eventually for our final robot we used larger wheels from the lab to get better traction and it also clearance for blocks to go under our chassis. 

One of the class milestones gave us trouble and took us a while to get a good range of frequencies for the colors to make sure it did not mistake blue, yellow, and black with each other. We also had to switch our QTI sensors out multiple times because some of them were not working even with us adding another 10 kOhm resistor and putting it closer to the board. As a result we decided not to use a color sensor on our final robot since there was no requirement on which side of the board we needed to end on. From this milestone we also added 20 kOhms resistance for each QTI sensor and adjusted the placement of the sensors themselves to be closer to the ground in hopes of the color sensing being as accurate as possible in different lighting settings. 

While working on the code for the competition we originally wanted our robot to continue driving around however sometimes when both the front QTI sensors sensed black our robot would start turning or it would pause not turn and then keep driving forward. We wanted to play it safe because we had not tested our robot on the board with Duffield lighting, so we changed the code so the robot would stop when both front QTI sensors detected black to ensure that our robot would not fall off the board because this would add a possibility of blocks falling out of our enclosure. 


## Competition Analysis
Our first 3 rounds did not go to plan since we did not check the voltage of the new battery we were given before the competition. As a result, the voltage was not high enough and our robot did not move at all or it would only slowly inch forward. Once we replaced the 9 V battery with a battery that was actually 9 V our robot ran as intended. Our robot successfully moved across the center of the board to collect blocks and would continue to drive around. We were pleasantly surprised with how the robot responded when in contact with the other robot. We thought our robot would be the one getting pushed, but our robot was actually robust enough to keep moving and eventually push the other robot out of the way. One thing that was not ideal, but not the end of the world, was that our two front QTI sensors would sometimes both sense black when only one was on black and thus stopping our robot. It would have been nice to keep driving around and potentially collect more blocks, but it was able to keep the initial blocks collected during our starting sequence in our robot perimeter. 


## Personal Contributions
