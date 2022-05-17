# Autonomous-Ball-Chaser
#### Introduction
This project is a simple example of how publishers and subscribers in ROS work, and the main mission of our autonomous vehicle here is to chase the white ball wherever it goes.

the project consists of two main nodes: drive_bot Node and ball_chaser Node
drive_bot : this node is responsible of publishing messages to the wheels joint angles.
ball_chaser: This client node will subscribe to the robot’s camera images and analyze them to determine the position of the white ball. Once the ball position is determined, the client node will request a service from the drive_bot server node to drive the robot toward the ball. The robot can drive either left, right or forward, depending on the robot position inside the image.
 
