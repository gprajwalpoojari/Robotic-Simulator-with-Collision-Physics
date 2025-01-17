# Robotic Simulator with Graphics and Collision Physics

## Demo
![simulator](https://github.com/gprajwalpoojari/Robotic_Simulator_with_Collision_Physics/assets/53962958/de21c61d-d099-43c3-b95c-b666eafea226)



## Some Background on Braitenberg Vehicle:
A Braitenberg vehicle is an agent that can autonomously move around based on its sensor inputs. It has primitive sensors that measure some stimulus at a point, and wheels (each driven by its own motor) that function as actuators or effectors. In the simplest configuration, a sensor is directly connected to an effector, so that a sensed signal immediately produces a movement of the wheel.

## The Braitenberg Vehicle implemented in this simulation:
This robotic Simulator implements a type of Braitenberg vehicle which has two “light sensors”. The more light received by the left light, the faster the right wheel turns. The more light received by the right light, the faster the left wheel turns. This will cause the vehicle to turn towards a light source, accelerating as it gets closer. The light sensors each point 60 degrees off from the robot’s forwards direction. So the left sensor will be theta + 60 degrees and the right sensor theta - 60 degrees.

A triangle poses a very nice shape to represent a robot because it is geometrically simple and has a clear forward orientation.

## About the environment:
The environment has been implemented from scratch using a bitmap image. This image file is displayed in the browser using the image server. The bitmap image consists of 3 fixed light sources shaped in the form of a square and positioned at different locations. The traingular shaped robot is initially spawned at the center of the bitmap image. Depending on the lights received by the sensors of the robot, the robot starts moving towards the region with greater light intensity. 

The environment looks like the following:

![](images/Initialize_world.bmp)

A collision detection code also checks for collision at each time step. Once the robot collides with the light source, the terminal window displays "collision!" indicating that the robot has collided with the light source.

To run the code, type the following command:
```
./braitenberg <timestep> <fast=0|1>
 ```
  
Here is an example simulation:
```
./braitenberg 500 0
```

https://user-images.githubusercontent.com/53962958/143908937-f4b58cdf-7e13-44aa-9e0a-8d74fbbd6fd5.mp4




## References
https://en.wikipedia.org/wiki/Braitenberg_vehicle

https://robotics.umich.edu/academic-program/courses/rob599-f19/homework2/
