# Autonomous-Ball-Chaser
### Introduction
This project is a simple example of how publishers and subscribers in ROS work, and the main mission of our autonomous vehicle here is to chase the white ball wherever it goes.
![Screenshot 2022-05-17 18 08 31](https://user-images.githubusercontent.com/105011124/168858230-52b0772d-cbc3-412e-b4ba-1d02a1462961.png)

the project consists of two main nodes: drive_bot Node and ball_chaser Node
drive_bot : this node is responsible of publishing messages to the wheels joint angles.
ball_chaser: This client node will subscribe to the robot’s camera images and analyze them to determine the position of the white ball. Once the ball position is determined, the client node will request a service from the drive_bot server node to drive the robot toward the ball. The robot can drive either left, right or forward, depending on the robot position inside the image.
 
