# Grasping System for Humanoid Robots

This project focuses on the design and implementation of a grasping system for unknown objects using a humanoid robot within the **QiBullet simulator**.  
The system enables a **Softbank Robotics Pepper robot** to detect, localize, and grasp objects without requiring additional markers or sensors beyond its default hardware.

---

## 🚀 Features

- **Object Detection**: Uses **YOLOv10** to identify and place bounding boxes around target objects in images captured by Pepper’s cameras.  
- **Monocular Depth Estimation**: Leverages **Depth Anything V2** to estimate object distances and generate a depth map.  
- **Coordinate Mapping**: Transforms image coordinates into Pepper’s base coordinate system to compute object positions in 3D space.  
- **Path Planning**: Implements an algorithm to generate an optimal path for the arm, adjusting position and orientation for the best grasp pose.  
- **Inverse Kinematics**: Uses the **Playful Kinematics framework** to compute joint configurations, considering both arm DOF (5 per arm) and lower body DOF.  
- **Robustness**: Achieved a **72% success rate** when grasping a small bottle in **25 simulated tests**.  
- **Modularity**: Easily adaptable to other humanoid robots thanks to modular implementation.

---

## ⚙️ Technical Specifications

- **Programming Language**: Python  
- **Test Environment**:  
  - Intel Core i9 CPU  
  - Nvidia RTX 4060 GPU  

---

## 🤖 Hardware and Simulation Environment

- **Robot Platform**: Softbank Robotics **Pepper**  
- **Degrees of Freedom (DOF)**:  
  - 20 DOF total  
  - 5 DOF per arm  
- **Cameras**:  
  - Two 2D stereo cameras (resolution: 640×480)  
  - Forehead camera: initial detection  
  - Mouth camera: close-up grasp planning  
- **Grasping Limitations**:  
  - Binary open/close hand motion (no finger articulation)  
  - Max payload: 200g  
  - Target object: small bottle adapted to Pepper’s limitations  
- **Simulator**: **QiBullet** (based on Bullet physics engine), chosen for realistic physics and environment simulation  

---

## 🎯 Project Goals and Contributions

The main goal is to enable the **Pepper robot**, which was not originally designed for precise grasping, to perform complex grasping tasks using **only its default sensors**.  

- Contributes to the state of the art by addressing grasping with humanoid robots similar to Pepper.  
- Demonstrates the feasibility of grasping strategies in simulation, reducing costs and risks compared to real-world testing.  
- Provides a modular pipeline that can be extended to other humanoid platforms.  

---
