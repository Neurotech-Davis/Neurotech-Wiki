By Priyal Patel for _Neurotech@Davis_

**Example: Robotic Arm Pipeline**

**Project Repo**

https://github.com/Neurotech-Davis/RoboticArm

**Materials**

- Emotiv Insight Pro Headset
- Laptop
- Wires
- Breadboard
- Arduino
- 3D Printed Robotic Arm Casing
- Servo Motors
- Batteries

**Context**

Emotiv has a pre-built mental command detection algorithm. To increase the accuracy of this algorithm for a particular participant, trainings were conducted and using these trainings the algorithm is able to form patterns in brain activity that match each mental command.

Trainings were conducted prior to assist the Emotiv's algorithm in detecting mental commands for our participant Grace Lim (Projects Member 2022-2024, Project's Board Co-Lead 2024-2025).

**Node-Red Toolbox Pipeline**

<img width="800" alt="node-red-flow" src="https://github.com/user-attachments/assets/07a59355-a171-4869-8ca6-034cf1221e5a">

**How did we create our Pipeline?**

1- Key Research Questions

What are the distinct components that we need to connect?

Data collected by the Emotiv headset, Emotiv's mental command detection algorithm, program to map mental commands to arm movement directions, Arduino board, and the robotic arm.

How to feed data collected by the Emotiv headset to Emotiv's mental command detection algorithm?

By examining Emotiv's website, we found two options: using Emotiv's API functions or using the Node-Red Toolbox. We first tried using the API, but needed special authorization information from paid features to access. Then, we pivoted to using the Node-Red Toolbox. The Emotiv website was missing some setup steps, so we leveraged video tutorials on youtube to assist us. After, we tested the software's functionality by mimicing examples we found online and were able to succesfully connect these two components.

How to map mental commands to arm movement directions?

We brainstormed and collectively agreed that the easiest way was to map the name of the command detected to a number; we choose to do this by creating python scripts that use serial connection communication to send the appropriate number to the Arduino. Node-Red Toolbox enabled us to have a separate node for each command that actived when detected; directly after the related python script node would activate causing this script to run, sending a number to the Arduino through a wired usb connection.

How to use the input the Arduino board will receive to make the robotic arm move?

A team member with hardware and circuits experience suggested using servo motors to achieve the rotating motion we desired for our robotic arm. We ran into the problem of the arm not being able to rotate enough and added extra batteries to power the motors. Using wired connections and a breadboard, we were able to connect a number for a mental command with a position for the servo motors.

2- Cost Analysis

How much do we want to spend on the project?

As little as possible...found a free online 3D cad design for the arm, used a team member's friend 3D printing to print for cheap, paid for servo motors, paid for batteries, used a team member's Arduino, used a team member's wiring/breadboard kit, used free software programs, used our Emotiv headset we won at OpenBCI Spring 2023 competition, and picked a project that could hopefully be completed in time for the April 2024 Neurotech Conference competition.

**Hardware Setup**

<img width="400" alt="hardwaresetup" src="https://github.com/user-attachments/assets/f8d44e46-ab60-4bcc-9f3d-3159aa3588c1">

**Results**

When everything connects, exciting things can happen...

<img src="https://github.com/user-attachments/assets/ddef32f0-1915-4129-921f-6974b1aaccd5" width="400">

Demo of the drop command with participant Grace

**Extras**

We are so excited to see all the cool ideas and amazing projects built by our fellow Neurotechies!

<img src="https://github.com/user-attachments/assets/0146e680-affd-49e7-8442-74634ccc68ef" width="200">







