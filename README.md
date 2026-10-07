<div align="center">

# Sharath N Payyadi

**Robotics Engineer · ROS 2 · Autonomous Mobile Robots · Robotic Manipulation · Sim-to-Real**

<a href="https://sharathnpayyadi.github.io/"><img src="https://img.shields.io/badge/Portfolio-sharathnpayyadi.github.io-0A66C2?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio"></a>
<a href="https://www.linkedin.com/in/sharath-n-payyadi/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="https://sharathnpayyadi.github.io/CV_Sharath_N_Payyadi.pdf"><img src="https://img.shields.io/badge/CV-Download-2E7D32?style=for-the-badge" alt="CV"></a>
<a href="https://medium.com/@sharathnpayyadi"><img src="https://img.shields.io/badge/Medium-Articles-000000?style=for-the-badge&logo=medium&logoColor=white" alt="Medium"></a>
<a href="mailto:sharathnpayyadi@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>

</div>

---

## About

I am a Robotics Engineer building ROS-based autonomy software for autonomous mobile robots (AMRs) and robotic arms. My work spans the full path from simulation to field deployment: developing ROS 1 / ROS 2 modules, validating them in NVIDIA Isaac Sim and Gazebo, building the CI/CD and Docker infrastructure around them, and supporting on-site commissioning through factory and site acceptance tests.

I am focused on reliable robotics software that scales from development to production, with a growing interest in robot learning through imitation learning and teleoperation.

## Core Expertise

- **Autonomous Navigation:** Nav2, AMCL localization, behavior trees, multi-waypoint mission execution
- **Manipulation & Motion Planning:** MoveIt, pick-and-place pipelines, coordinated mobile-base and arm execution
- **Multi-Robot Systems:** graph-based traffic management, deadlock avoidance, shared path allocation
- **Perception:** camera-based object detection (YOLO, OpenCV), pose estimation, LiDAR and IMU integration
- **Simulation & Sim-to-Real:** NVIDIA Isaac Sim, Isaac Lab, Gazebo, simulation-first validation workflows
- **Robotics Infrastructure:** Dockerized ROS stacks, Jenkins CI/CD, testing pipelines, deployment and commissioning

## Projects

### Robotics & AI

#### iw_hub Autonomous Pick-and-Place
End-to-end autonomous mission stack for the idealworks iw_hub AMR in NVIDIA Isaac Sim. A single ROS 2 service runs the full mission (navigate, lift, transport, lower, clear) with Nav2 + AMCL on a dual-LiDAR base, velocity-ramped lift control, and a rosbridge web dashboard.
<br>`ROS 2 Humble` `Nav2` `Isaac Sim` `AMR` `rosbridge` · [GitHub](https://github.com/SHARATHNPAYYADI/iw_hub_isaac_ws)

#### Husky Autonomous Inspection Robot
Simulation-first inspection stack for a Clearpath Husky UGV. A BehaviorTree.CPP mission runner loops navigate, inspect and report across waypoints, with YOLO-based fire-extinguisher detection, auto-generated inspection reports, and a FastAPI dashboard for teleoperation and mission control.
<br>`ROS 2` `Nav2` `BehaviorTree.CPP` `YOLO` `Gazebo` · [GitHub](https://github.com/SHARATHNPAYYADI/husky_ai_inspection)

#### Husky Digital Twin
Browser-native 3D digital twin of a warehouse robot with real-time tracking, 8-directional A* pathfinding with live replanning around obstacles, a layout editor, multi-stop task queue, and persistent run metrics.
<br>`FastAPI` `React Three Fiber` `TypeScript` `WebSocket` · [GitHub](https://github.com/SHARATHNPAYYADI/husky-twin) · [Live demo](https://husky-twin.vercel.app)

#### Multi-Robot Traffic Management on a Graph Environment (Master's thesis)
Centralized traffic manager for heterogeneous AMR fleets, built with NODE Robotics. Models the site as a topological graph, detects path conflicts ahead of time, generates detours or safe waiting strategies, and dispatches orders to robots over VDA5050 / MQTT. Validated across detour, wait, merge and cross scenarios with zero deadlocks.
<br>`ROS 2` `C++` `VDA5050` `MQTT` `Fleet Management`

#### Vision-Based Pick-and-Place with TIAGo
Autonomous pick-and-place pipeline for the PAL Robotics TIAGo mobile manipulator: ArUco-based pose estimation from the head RGB-D camera, Octomap collision mapping, spherical grasp sampling and MoveIt motion planning. Validated in Gazebo and on the physical robot.
<br>`ROS` `MoveIt` `OpenCV / ArUco` `Octomap` `Gazebo`

#### Franka Panda Manipulation Workspace
ROS 2 workspace for the Franka Emika Panda arm in Gazebo with MoveIt 2. Includes simple and camera-based pick-and-place demos, a pick-and-insert scenario (spark plug into socket), teleoperation and trajectory following, OpenCV colour-based object pose estimation, custom service interfaces, and unit plus integration tests for detection, planning and grasping.
<br>`ROS 2 Humble` `MoveIt 2` `Gazebo` `OpenCV` `Python` `colcon test` · [GitHub](https://github.com/SHARATHNPAYYADI/panda_ws)

#### Differential Drive Robot: Localization & Sensor Fusion
Differential drive robot with 2D LiDAR, IMU and wheel odometry, simulated in an apartment-style Gazebo world. Analyses wheel-odometry drift against ground truth and LiDAR scan-matching poses, then fuses odometry and scan-based corrections with a custom Extended Kalman Filter, with trajectory recording and plotting tools.
<br>`ROS 2` `Gazebo` `LiDAR` `IMU` `EKF` `Python` · [GitHub](https://github.com/SHARATHNPAYYADI/diff_drive_ws)

### Embedded Systems

#### Disease Detection in Paddy Crop using CNN (Bachelor's thesis)
Portable crop-monitoring device on a Raspberry Pi that captures leaf images with a Pi Camera, runs two CNN models to detect rice blast and bacterial blight (about 95% overall accuracy), and alerts the farmer by SMS through a GSM module, with no internet connection required. Published in IJRTE (2020).
<br>`Raspberry Pi` `Pi Camera` `GSM` `Keras / TensorFlow` `CNN` `Python` · [Paper](https://www.ijrte.org/portfolio-item/f9835038620/)

## Technical Stack

**Languages**<br>
![C++](https://img.shields.io/badge/C++17-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

**Robotics**<br>
![ROS 2](https://img.shields.io/badge/ROS%201%20%2F%20ROS%202-22314E?style=flat-square&logo=ros&logoColor=white)
![Nav2](https://img.shields.io/badge/Nav2-22314E?style=flat-square)
![MoveIt](https://img.shields.io/badge/MoveIt-22314E?style=flat-square)
![BehaviorTree.CPP](https://img.shields.io/badge/BehaviorTree.CPP-22314E?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO-111F68?style=flat-square)

**Simulation**<br>
![Isaac Sim](https://img.shields.io/badge/NVIDIA%20Isaac%20Sim-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Isaac Lab](https://img.shields.io/badge/Isaac%20Lab-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Gazebo](https://img.shields.io/badge/Gazebo-F58113?style=flat-square)

**AI & Embedded**<br>
![TensorFlow](https://img.shields.io/badge/TensorFlow%20%2F%20Keras-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)

**DevOps & Tools**<br>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

---

<div align="center">

**Open to collaboration on autonomous systems, sim-to-real and multi-robot robotics.**<br>
Reach me at [sharathnpayyadi@gmail.com](mailto:sharathnpayyadi@gmail.com) or on [LinkedIn](https://www.linkedin.com/in/sharath-n-payyadi/).

</div>
