By Priyal Patel for _Neurotech@Davis_

**Example: Robotic Arm Pipeline**

**Project Repo**

https://github.com/Neurotech-Davis/RoboticArm

**Materials**

- Emotiv Insight Pro Headset
- Laptop
- Wires
- Bread Board
- Arduino
- 3D Printed Robotic Arm Casing
- Servo Motors
- Batteries

**Context**

Emotiv has a pre-built mental command detection algorithm. To increase the accuracy of this algorithm for a particular participant, trainings were conducted and using these trainings the algorithm is able to form patterns in brain activity that match each mental command.

Trainings were conducted prior to create a set of training to assist the Emotiv's algorithm in detecting mental commands for our participant Grace Lim (Projects Member 2022-2024, Project's Board Co-Lead 2024-2025).

**How did we create our Pipeline?**

1- Key Research Questions

What are the distinct components that we need to connect?

Data collected by the Emotiv headset, Emotiv's mental command detection algorithm, program to map mental commands to arm movement directions, Arduino board, and the robotic arm.

How to feed data collected by the Emotiv headset to Emotiv's mental command detection algorithm?

By examining Emotiv's website, we found two options: using Emotiv's API functions or using the Node-Red Toolbox. We first tried using the API, but needed special authorization information from paid features to access. Then, we pivoted to using the Node-Red Toolbox. This was a difficult process to setup; we leveraged video tutorials on youtube to assist us. After, we tested the software's functionality by mimicing examples we found online and were able to succesfully connect these two components.

How to map mental commands to arm movement directions?

We brainstormed and collectively agreed that the easiest way was to map the name of the command detected to a number; we choose to do this by creating python scripts that use serial connection communication to send the appropriate number to the Arduino. Node-Red Toolbox enabled us to have a separate node for each command to active when detected; directly after the according python script node would activate causing this script to run and cause a number to be sent to the Arduino.

How to connect the input Arduino board will receive to make the robotic arm move?

TODO: need to finish

2- Hardware Materials Brainstorm

TODO: need to finish

3- Cost Analysis
How much do we want to spent on the project?
As little as possible...found a free online 3D cad design for the arm, use team member's friend 3D printing to print for cheap, picked servo motors, used team member's wiring/bread board kit, used free software programs, used free hardware we won at OpenBCI Spring 2023 competition, and picked project that could be hopefully be completed in time for the April 2024 Neurotech Conference competition.