# UVC-Disinfection-Robot
Design and Simulation of UVC Disinfection Robot using ROS

## Softwares Used
**Robot Operating System(ROS)**  
**Fusion 360**  
**Gazebo**  
**Rviz**

https://user-images.githubusercontent.com/72541715/127963867-d864738a-9dbb-4577-a7b6-3873478fa4e3.mp4

## About ROS
The **Robot Operating System (ROS)** is a flexible framework for writing robot software. It is a collection of tools, libraries, and conventions that aim to simplify the task of creating complex and robust robot behavior across a wide variety of robotic platforms.

## Robot Model Designed in FUSION 360

![Fusion Model](https://user-images.githubusercontent.com/72541715/127964696-bbcaf687-6e80-4ecf-94de-86eb9522bd19.png)

## World for Robot Simulation
The world for robot simulation is designed to include various real-world obstacles so that the robot won't encounter any real-time working errors. The **Hospital** world is designed using **Gazebo Building Editor**.

![Hospital World](https://user-images.githubusercontent.com/72541715/127981025-58960507-bddc-4351-a5f5-c162f94fa0e7.png)


## Movement of Robot in the world
The movements of the robot in Hospital World are controlled using the ROS package **teleop_twist_keyboard**.

## SLAM using Gmapping
A 2D map of the hospital world is built with the help of **lidar sensor** mounted on the Robot. The map is build using the ROS package **gmapping** which provides a laser-based SLAM.

![Hospital World Map](https://user-images.githubusercontent.com/72541715/127989474-7784b17f-5f2e-40e1-9c14-7a39d2edd2d6.png)

## Autonomous Navigation
Autonomous Navigation of the Robot is achieved using the ROS **navigation-stack** package. This package helps to move the robot from the initial position to the goal position, without making any collision with the environment.

It involves the robot localising itself on the static map using the AMCL package which uses the Adaptive Monte Carlo localization algorithm. After we obtain the robot’s current position, the goal position is sent to the move_base node which will then send it to the global planner to plan the entire path whose each segment is then executed by the local planner, which is associated with the local costmap. This is followed by it generating command velocity in the form of a twist message to the robot base controller which then converts it to the equivalent motor speed.

![image](https://user-images.githubusercontent.com/72541715/127992054-66f77875-8dbf-40de-90e1-812f18b03f6c.png)
