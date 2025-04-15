# 🤖 Gesture Control Publisher for TurtleBot (MediaPipe + ROS 2 + Gazebo)

This project allows you to control a **TurtleBot in Gazebo** using **hand gestures**, captured via your webcam and interpreted using **MediaPipe** in a Jupyter Notebook. This repository is **only responsible for detecting gestures and publishing direction commands**, which are then received by a ROS 2 node that moves the TurtleBot accordingly.

---

## 🪄 How It Works

1. **MediaPipe** is used to detect and classify hand gestures in real-time using your webcam.
2. Based on specific hand gestures (like open palm, fist, etc.), the notebook publishes direction commands like:
   - `forward`
   - `backward`
   - `left`
   - `right`
   - `stop`
3. These commands are published to a ROS 2 topic (e.g., `/gesture_direction`).
4. A separate ROS 2 Python script  subscribes to that topic and moves the TurtleBot in Gazebo accordingly.
