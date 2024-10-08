By Priyal Patel for _Neurotech@Davis_

**Adding Hardware**

Let's say you want to map the output from the algorithm or machine learning model to make a light flash or make an object move in a certain direction.

So how do you actually do that?

Using hardware ^\_^

There are many different ways to accomplish these tasks, but one way we have used in the past is connecting an Arduino to motors, lights, or other pieces of hardware.

**How does this work?**

1- Create desired input and output mappings

Using a special software language, you can write an instruction set for the arduino to follow that details how to process the input it will receive and what to output. Using a wired usb connection, these instructions are loaded into the Arduino board.

2- Connect output of Arduino board to other hardware

Let's say we are using servo motors. There will be a wire connected to the arduino board to a bigger board and a wire from this board to the servo motor. Servo motors are special because they will rotate a certain amount based on the input received through a wire.

3- Send the output from the computer program to the Arduino board

Using a wired usb connection, the computer can send the output from an algorithm or ML model to the Arduino board. The input will be read and based on the Arduino's instructions a certain position will be sent through a wire to the servo motor.

4- Move an object by rotating the motor

Based on the input received, the servo motor will rotate to this position. There is another wire connected to the motor and another object; this will cause the object to move simultaneously while the motor is rotating.
