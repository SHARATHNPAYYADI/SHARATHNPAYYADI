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

I am focused on reliable robotics software that scales from development to production, with a growing interest in robot learning through imitation learning and teleoperation. I am currently working on an **agentic AI** project.

## Core Expertise

- **Autonomous Navigation:** Nav2, AMCL localization, behavior trees, multi-waypoint mission execution
- **Manipulation & Motion Planning:** MoveIt, pick-and-place pipelines, coordinated mobile-base and arm execution
- **Multi-Robot Systems:** graph-based traffic management, deadlock avoidance, shared path allocation
- **Perception:** camera-based object detection (YOLO, OpenCV), pose estimation, LiDAR and IMU integration
- **Simulation & Sim-to-Real:** NVIDIA Isaac Sim, Isaac Lab, Gazebo, Unity, simulation-first validation workflows
- **Robotics Infrastructure:** Dockerized ROS stacks, Jenkins CI/CD, testing pipelines, deployment and commissioning

## Projects

### Robotics & AI

#### iw_hub Autonomous Pick-and-Place
End-to-end autonomous navigation and pick-and-place stack for the idealworks iw_hub AMR, simulated in NVIDIA Isaac Sim and driven entirely through ROS 2 Humble + Nav2.
- One `/mission` service call runs the full sequence: navigate, lift the dolly, transport, lower, clear
- Nav2 + AMCL on a dual-LiDAR diff-drive base, with the map generated from Isaac Sim's Occupancy Map tool
- Velocity-ramped scissor-lift control at 50 Hz for smooth dolly pickup without destabilizing the load
- Browser dashboard over rosbridge for mission triggering and live lift/pose telemetry

`ROS 2 Humble` `Nav2` `Isaac Sim` `SLAM Toolbox` `rosbridge` `Python`<br>
[GitHub](https://github.com/SHARATHNPAYYADI/iw_hub_isaac_ws) · [Project details](https://sharathnpayyadi.github.io/projects/iw-hub-pick-place.html)

#### Husky Autonomous Inspection Robot
Simulation-first inspection stack for the Clearpath Husky UGV on a custom Gazebo construction-site world.
- BehaviorTree.CPP mission runner loops navigate, capture, inspect and report across 5 waypoints from one service call
- YOLO fire-extinguisher detection at every waypoint, flagging each point as found or missing
- Auto-generated HTML inspection report at the end of each mission
- FastAPI + web dashboard with virtual-joystick teleop over WebSocket and live mission telemetry

`ROS 2 Humble` `Nav2` `AMCL` `BehaviorTree.CPP` `YOLO` `Gazebo` `FastAPI`<br>
[GitHub](https://github.com/SHARATHNPAYYADI/husky_ai_inspection) · [Live demo](https://sharathnpayyadi.github.io/projects/husky-inspection-demo.html) · [Project details](https://sharathnpayyadi.github.io/projects/husky-inspection.html)

#### Husky Digital Twin
Browser-native 3D digital twin of a warehouse Husky with no ROS and no physics engine: a deterministic Python asyncio tick loop synced live to a React Three Fiber scene.
- 8-directional A* pathfinding on a 40×40 grid with live replanning around dropped pallets and wandering people
- Multi-stop routes with per-stop reports (duration, distance, replans, obstacles hit)
- Warehouse layout editor with hot-swappable saved layouts and an onboard robot camera view
- Run history persisted to SQLite and browsable in a metrics dashboard; ~100 ms WebSocket sync

`FastAPI` `React Three Fiber` `TypeScript` `WebSocket` `SQLite`<br>
[GitHub](https://github.com/SHARATHNPAYYADI/husky-twin) · [Live demo](https://husky-twin.vercel.app) · [Project details](https://sharathnpayyadi.github.io/projects/husky-twin.html)

#### Multi-Robot Traffic Management on a Graph Environment (Master's thesis)
Centralized traffic manager for heterogeneous AMR fleets, developed at NODE Robotics (Fraunhofer IPA spin-off) with Hochschule Darmstadt.
- Models the site as a topological graph of sections, corridors and crossings with traffic rules (one-way / two-way)
- Detects path conflicts ahead of time and generates detours, or falls back to waiting at the nearest safe spot
- Dispatches orders to robot fleets over the VDA5050 standard via MQTT
- Validated on detour, wait, merge and cross scenarios with zero deadlocks; implemented in C++ with Google Tests in CI

`ROS 2` `C++` `VDA5050` `MQTT` `Fleet Management` `Path Planning`<br>
[Project details](https://sharathnpayyadi.github.io/projects/thesis.html) · [Thesis report](https://sharathnpayyadi.github.io/reports/master_thesis.pdf)

#### Vision-Based Pick-and-Place with TIAGo
Autonomous pick-and-place pipeline for the PAL Robotics TIAGo, a 12-DoF mobile manipulator, at the Hochschule Darmstadt robotics lab.
- ArUco marker detection and 6-DoF pose estimation from the head RGB-D camera
- Octomap collision world rebuilt around the table and object before every grasp
- Spherical grasp sampling with MoveIt (OMPL) collision-aware motion planning
- Validated both in Gazebo simulation and on the physical robot

`ROS` `MoveIt` `OpenCV / ArUco` `Octomap` `Gazebo` `Python`<br>
[Project details](https://sharathnpayyadi.github.io/projects/tiago-project.html) · [Project report](https://sharathnpayyadi.github.io/reports/tiago_project_report.pdf)

#### Franka Panda Manipulation Workspace
ROS 2 workspace for the Franka Emika Panda arm in Gazebo with MoveIt 2.
- Simple and camera-based pick-and-place demos, plus a pick-and-insert scenario (spark plug into socket)
- OpenCV colour-based object pose estimation
- Teleoperation and trajectory-following examples with custom service interfaces
- Unit and integration tests for detection, motion planning and grasping

`ROS 2 Humble` `MoveIt 2` `Gazebo` `OpenCV` `Python` `colcon test`<br>
[GitHub](https://github.com/SHARATHNPAYYADI/panda_ws)

#### Differential Drive Robot: Localization & Sensor Fusion
Differential drive robot with 2D LiDAR, IMU and wheel odometry in an apartment-style Gazebo world.
- Sensor verification in RViz and a full TF tree for the robot
- Odometry drift analysis against ground truth and LiDAR scan-matching poses
- Custom Extended Kalman Filter fusing wheel odometry with scan-based corrections, plus trajectory recording and plotting tools

`ROS 2` `Gazebo` `LiDAR` `IMU` `EKF` `Python`<br>
[GitHub](https://github.com/SHARATHNPAYYADI/diff_drive_ws)

### Embedded Systems

#### Disease Detection in Paddy Crop using CNN (Bachelor's thesis)
Portable, offline crop-monitoring device that detects rice blast and bacterial blight from leaf images and alerts the farmer by SMS.
- Raspberry Pi 3 with Pi Camera capturing a leaf image every 30 minutes
- Two Keras CNN models (blast 96.8%, blight 95.5%; about 95% overall) running on the device
- GSM module sends the alert with a suggested remedy, so no internet connection is needed
- Published in IJRTE, Vol. 8 Issue 6, March 2020

`Raspberry Pi` `Pi Camera` `GSM` `Keras / TensorFlow` `CNN` `Python`<br>
[Project details](https://sharathnpayyadi.github.io/projects/bachelor_thesis.html) · [Paper](https://www.ijrte.org/portfolio-item/f9835038620/)

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
![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white)

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
