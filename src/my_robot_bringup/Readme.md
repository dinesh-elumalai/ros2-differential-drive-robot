# 🤖 ROS2 Differential Drive Robot (Gazebo Simulation)

This project demonstrates a **differential drive mobile robot** built using **ROS2 Jazzy**, simulated in Gazebo, and visualized in RViz.
The robot includes a **camera sensor** and supports **velocity control using /cmd_vel**.

---

## 🚀 Features

* 🧩 Robot modeled using **URDF/Xacro**
* 🎮 Differential drive control using `/cmd_vel`
* 📷 Camera sensor simulation
* 🌍 Gazebo physics simulation
* 🔗 ROS–Gazebo bridge integration
* 🧭 TF tree and robot state publishing
* 📊 RViz visualization

---

## 📂 Project Structure

```
ros2_ws/
 ├── src/
 │   ├── my_robot_description/
 │   │    ├── urdf/
 │   │    ├── launch/
 │   │    └── rviz/
 │   │
 │   └── my_robot_bringup/
 │        ├── launch/
 │        └── config/
 │             └── gazebo_bridge.yaml
```

---

## ⚙️ Requirements

* ROS2 Jazzy
* Gazebo Harmonic
* ros_gz_bridge
* rviz2

---

## 🛠️ Installation & Build

```bash
cd ~/ros2_ws
colcon build
source install/setup.bash
```

---

## ▶️ Run Simulation

```bash
ros2 launch my_robot_bringup my_robot_gazebo.launch.xml
```

---

## 🎮 Control the Robot

Move the robot using:

```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist "{linear: {x: 0.5}, angular: {z: 0.0}}"
```

---

## 📷 View Camera Output

Install viewer:

```bash
sudo apt install ros-jazzy-rqt-image-view
```

Run:

```bash
rqt_image_view
```

Select topic:

```
/camera/image_raw
```

---

## 🧠 Concepts Used

* Differential Drive Kinematics
* URDF / Xacro Modeling
* ROS2 Nodes, Topics, and Messages
* TF (Transform Tree)
* Gazebo Simulation
* Sensor Integration (Camera)

---

## 📸 Demo (Optional)

*Add screenshots of Gazebo and RViz here*

---

## 👨‍💻 Author

**Dinesh Elumalai**
Robotics Student – École Centrale de Nantes (ECN)

---

## ⭐ Future Improvements

* Add LiDAR sensor
* Implement SLAM (mapping)
* Autonomous navigation
* Computer vision integration

---
