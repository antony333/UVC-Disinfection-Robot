# UVC-Disinfection-Robot
Design and Simulation of UVC Disinfection Robot using ROS

https://user-images.githubusercontent.com/72541715/127963867-d864738a-9dbb-4577-a7b6-3873478fa4e3.mp4

## About ROS
The **Robot Operating System (ROS)** is a flexible framework for writing robot software. It is a collection of tools, libraries, and conventions that aim to simplify the task of creating complex and robust robot behavior across a wide variety of robotic platforms

## Robot Model Designed in FUSION 360

![Fusion Model](https://user-images.githubusercontent.com/72541715/127964696-bbcaf687-6e80-4ecf-94de-86eb9522bd19.png)

## World for Robot Simulation
The world for robot simulation is designed including various real-world obstacles so that robot won't encounter any real time working errors.The **Hospital** world is designed using **Gazebo Building Editor**.

![Hospital World](https://user-images.githubusercontent.com/72541715/127981025-58960507-bddc-4351-a5f5-c162f94fa0e7.png)


## Movement of Robot in the world
Movement of the robot in Hospital World is controlled using the ROS package **teleop_twist_keyboard**.

## SLAM using Gmapping
A 2D map of hospital world is build with the help of **lidar sensor** mounted on the Robot. The map is build using the ROS package **gmapping** which provides a laser based SLAM.

![Hospital World Map](https://user-images.githubusercontent.com/72541715/127989474-7784b17f-5f2e-40e1-9c14-7a39d2edd2d6.png=100x100)
