# Autonomous Electrified Vehicle (AEV)

- Developed algorithms for autonomous driving, enabling real-time obstacle detection, navigation, and path planning.
- Developed a control node in ROS to process depth camera messages, applying a pinhole camera model to calculate the Cartesian coordinates of obstacles within the camera’s frame
- Conducted analysis on the magnetic and electrical characteristics of electric motor drives.

## 🔧 **Overview**

Built and tested an Autonomous Electrified Vehicle (AEV) platform integrating VESC motor control, ROS-based navigation, LiDAR perception, and autonomous driving algorithms. Responsible for motor tuning, data logging, ROS driver modifications, and implementing collision-avoidance and navigation logic.

---

# ⚡ **Motor Control & VESC Work**

- Configured VESC parameters for direction control, PID speed regulation, and FOC tuning.
- Performed **speed-command tests** (2500/5000/7500 rpm) and **duty-cycle tests** (0.10–0.20).

- Logged and plotted **RPM**, **q-axis current**, and **d/q-axis voltages** for performance analysis.
- Demonstrated differences between **speed control (regulated)** vs **duty cycle control (raw voltage)**.

---

# 🤖 **ROS Development**

- Modified VESC ROS driver to extract and publish **q-axis torque-producing current**.
- Added new parsing functions using byte shifts & static_cast logic in C++.
- Updated CMake, launch files, and serial port configuration for Jetson Nano integration.
- Published motor commands via ROS topics and automated speed commands through scripts.

---

# 🎮 **Control Nodes**

- Tuned joystick → motor mapping in **JoyControl.py** (multiplier, control mode).
- Implemented steering mapping in **ServoControl.py** for servo angle control.

---

# 🗺️ **Localization, LiDAR & SLAM**

- Worked with LiDAR scan topics, TF frames, and SLAM mapping in RViz.
- Integrated IMU + wheel odometry for improved localization accuracy.
- Debugged scan matching issues and updated keyframe distance parameters.
- Visualized hallway mapping and analyzed drift/error sources.

---

# 🚙 **Autonomous Driving Algorithm**

- Implemented collision-avoidance assistance using LiDAR potential-field forces.
- Developed finite-state machine for **normal → backup → turn** behavior.
- Tuned parameters affecting steering, velocity decay, safe distance, and obstacle thresholds.
- Compared two optimization formulations for virtual barrier generation.

---

# 📊 **Tools & Technologies**

**ROS (melodic/noetic)** • Python • C++ • VESC Tool • Jetson Nano • LiDAR

**RViz** • SLAM • TF frames • FOC motor control • PID tuning • CSV logging & plotting

