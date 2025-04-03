# Autonomous Skid-Steer Robot 🤖

(Using Ultrasonic, IMU, Mono Camera,Camera, 2D & 3D LiDAR)




## 📌 Overview

This project is an autonomous skid-steer robot equipped with:

- **2D Lidar (A2 RPLIDAR):** Provides 360-degree distance measurements to create a 2D map of the robot’s surroundings, essential for obstacle detection and mapping.
- **Camera (RealSense D435):** Captures depth and color images for advanced perception tasks, including object recognition and spatial understanding.
- **IMU (MPU 6050):** Measures acceleration and angular velocity to provide orientation and movement data, crucial for stabilization and navigation.
- **Ultrasonic Sensor (HC-SR04):** Uses sound waves to measure distance to nearby objects, useful for collision avoidance and distance sensing.
- **Mono Camera** (object detection & visual navigation)
- **3D LiDAR** (high-resolution 3D perception)

Built using ROS (Robot Operating System) for sensor fusion and navigation.


## ⚙️ Dependencies

    ROS Noetic 

    Python 3.8+

    rplidar_ros (for 2D LiDAR)

    realsense-ros (if using Intel RealSense)

## 🚀 Installation

### Clone the repository:
    
    git clone https://github.com/KhaledGhandour/skid-steer-robot.git
    cd skid-steer-robot

### Install dependencies:

    sudo apt install ros-noetic-rplidar-ros ros-noetic-teleop-twist-keyboard
    pip install -r requirements.txt

### Run the ROS launch file:

    roslaunch skid_steer_robot robot_description.launch



## 🔧 Key Algorithms

### Feature                         Algorithm                                    Description

- **Obstacle Avoidance**            **RRT (Rapidly-exploring Random Tree)**	    **Uses LiDAR + Ultrasonic data**

- **Object Detection**	              **YOLOv5 / SSD**                          **Processes mono camera feed**

- **SLAM**                          **Gmapping / Cartographer**	                     **2D LiDAR-based mapping**

- **3D Perception**                  **PCL (Point Cloud Library)**                   **Processes 3D LiDAR data**
