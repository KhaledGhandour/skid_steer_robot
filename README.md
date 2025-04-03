#Autonomous Skid-Steer Robot 🤖

(Using Ultrasonic, IMU, Mono Camera,Camera, 2D & 3D LiDAR)




##📌 Overview

This project is an autonomous skid-steer robot equipped with:

    Ultrasonic sensors (obstacle avoidance)

    IMU (inertial measurement for orientation & acceleration)

    Mono Camera (object detection & visual navigation)

    2D LiDAR (SLAM & environment mapping)

    3D LiDAR (high-resolution 3D perception)

Built using ROS (Robot Operating System) for sensor fusion and navigation.


##⚙️ Dependencies

    ROS Noetic 

    Python 3.8+

    rplidar_ros (for 2D LiDAR)

    realsense-ros (if using Intel RealSense)

##🚀 Installation

    ###Clone the repository:
    
    git clone https://github.com/KhaledGhandour/skid-steer-robot.git
    cd skid-steer-robot

    ###Install dependencies:

    sudo apt install ros-noetic-rplidar-ros ros-noetic-teleop-twist-keyboard
    pip install -r requirements.txt

    ###Run the ROS launch file:

    roslaunch skid_steer_robot robot_description.launch



##🔧 Key Algorithms

#Feature                         #Algorithm                                    #Description

Obstacle Avoidance	            RRT (Rapidly-exploring Random Tree)	         Uses LiDAR + Ultrasonic data

Object Detection	              YOLOv5 / SSD	                               Processes mono camera feed

SLAM	                          Gmapping / Cartographer	                     2D LiDAR-based mapping

3D Perception	                  PCL (Point Cloud Library)	                   Processes 3D LiDAR data
