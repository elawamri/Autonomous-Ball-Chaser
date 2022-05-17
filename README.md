# Autonomous-Ball-Chaser
## Introduction
This project is a simple example of how publishers and subscribers in ROS work, and the main mission of our autonomous vehicle here is to chase the white ball wherever it goes,the project consists of two main nodes: drive_bot and process_images.

![Screenshot 2022-05-17 18 08 31](https://user-images.githubusercontent.com/105011124/168858230-52b0772d-cbc3-412e-b4ba-1d02a1462961.png)

### 1. drive_bot
This node is responsible of publishing messages to the wheels joint angles.
### 2. process_images
This client node will subscribe to the robot’s camera images and analyze them to determine the position of the white ball. Once the ball position is determined, the client node will request a service from the ```drive_bot``` server node to drive the robot toward the ball. The robot can drive either left, right or forward, depending on the robot position inside the image
## Robot's Test.
First, place files in your catkin workspace.
### 1. Launch the robot inside your world
```bash
$ cd /home/workspace/catkin_ws/
$ source devel/setup.bash
$ roslaunch my_robot world.launch
```
### 2. Run ```drive_bot``` and ```process_image```
This can be done by executing ```ball_chaser.launch```:
```bash
$ cd /home/workspace/catkin_ws/
$ source devel/setup.bash
$ roslaunch ball_chaser ball_chaser.launch
```
### 3. Visualize
To visualize the robot’s camera images, you can subscribe to camera RGB image topic from RViz. Or you can run the ```rqt_image_view node```:
```bash
$ cd /home/workspace/catkin_ws/
$ source devel/setup.bash
$ rosrun rqt_image_view rqt_image_view
```
### 4. Preview
Now place the white ball at different positions in front of the robot and see if the robot is capable of chasing the ball , you can see a full video preview [here](https://www.youtube.com/watch?v=DOmrBtTaV24).


 
