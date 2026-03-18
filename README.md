# ros2-differential-drive-robot
# 🤖 ROS2 Differential Drive Robot (Gazebo + RViz)

A complete simulation of a **differential drive mobile robot** using **ROS2 Jazzy**, featuring **Gazebo simulation**, **RViz visualization**, and **camera sensor integration**.

---

## 🚀 Features

* Differential drive robot model using **Xacro**
* Real-time simulation in **Gazebo**
* Visualization in **RViz**
* Velocity control using `/cmd_vel`
* Camera sensor integration
* Modular ROS2 package structure:

  * `my_robot_description`
  * `my_robot_bringup`

---

## 🛠️ Technologies Used

* ROS2 Jazzy
* Gazebo
* RViz2
* Xacro (URDF macros)
* Python (launch files)
* YAML (configuration)

---

## 📁 Project Structure

```
ros2-differential-drive-robot/
├── src/
│   ├── my_robot_description/
│   │   ├── urdf/
│   │   ├── rviz/
│   │   ├── launch/
│   │   └── package.xml
│   ├── my_robot_bringup/
│   │   ├── launch/
│   │   ├── config/
│   │   ├── worlds/
│   │   └── package.xml
├── README.md
```

---

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/dinesh-elumalai/ros2-differential-drive-robot.git
cd ros2-differential-drive-robot
```

### 2. Build the workspace

```bash
colcon build
```

### 3. Source the workspace

```bash
source install/setup.bash
```

---

## ▶️ Run the Simulation

```bash
ros2 launch my_robot_bringup my_robot_gazebo.launch.xml
```

---

## 🎮 Control the Robot

Use the `/cmd_vel` topic to control the robot:

```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist "{linear: {x: 0.5}, angular: {z: 0.0}}"
```

---

## 📷 Visualization

* **Gazebo** → Robot simulation environment
* **RViz** → Robot model and sensor visualization

---

## 🧠 Architecture Overview

* `my_robot_description`

  * Defines robot using **URDF/Xacro**
  * Includes camera and base model
* `my_robot_bringup`

  * Launches Gazebo world
  * Loads robot model
  * Starts simulation and controllers

---

## 📌 Future Improvements

* SLAM (Simultaneous Localization and Mapping)
* Autonomous navigation (Nav2)
* Obstacle avoidance
* Sensor fusion (IMU, LiDAR)

---

## 👨‍💻 Author

**Dinesh Elumalai**
Robotics Student | ROS2 Developer

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and feel free to contribute!
