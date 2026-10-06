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

#### [iw_hub Autonomous Pick-and-Place](https://github.com/SHARATHNPAYYADI/iw_hub_isaac_ws)
End-to-end autonomous mission stack for the idealworks iw_hub AMR in NVIDIA Isaac Sim. A single ROS 2 service runs the full mission (navigate, lift, transport, lower, clear) with Nav2 + AMCL on a dual-LiDAR base, velocity-ramped lift control, and a rosbridge web dashboard.
<br>`ROS 2 Humble` `Nav2` `Isaac Sim` `AMR` `rosbridge` · [Project details](https://sharathnpayyadi.github.io/projects/iw-hub-pick-place.html)

#### [Husky Autonomous Inspection Robot](https://github.com/SHARATHNPAYYADI/husky_ai_inspection)
Simulation-first inspection stack for a Clearpath Husky UGV. A BehaviorTree.CPP mission runner loops navigate, inspect and report across waypoints, with YOLO-based fire-extinguisher detection, auto-generated inspection reports, and a FastAPI dashboard for teleoperation and mission control.
<br>`ROS 2` `Nav2` `BehaviorTree.CPP` `YOLO` `Gazebo` · [Live demo](https://sharathnpayyadi.github.io/projects/husky-inspection-demo.html) · [Project details](https://sharathnpayyadi.github.io/projects/husky-inspection.html)

#### [Husky Digital Twin](https://github.com/SHARATHNPAYYADI/husky-twin)
Browser-native 3D digital twin of a warehouse robot with real-time tracking, 8-directional A* pathfinding with live replanning around obstacles, a layout editor, multi-stop task queue, and persistent run metrics.
<br>`FastAPI` `React Three Fiber` `TypeScript` `WebSocket` · [Live demo](https://husky-twin.vercel.app) · [Project details](https://sharathnpayyadi.github.io/projects/husky-twin.html)

#### Academic research
- **[Traffic Management of Multiple Robots using a Graph Environment](https://sharathnpayyadi.github.io/projects/thesis.html)** (Master's thesis): priority-based scheduling and shared path allocation for multi-robot fleets, validated in ROS simulation. [Report](https://sharathnpayyadi.github.io/reports/master_thesis.pdf)
- **[Vision-Based Pick-and-Place with the TIAGo Robot](https://sharathnpayyadi.github.io/projects/tiago-project.html)**: object detection integrated with MoveIt motion planning on a mobile manipulator. [Report](https://sharathnpayyadi.github.io/reports/tiago_project_report.pdf)
- **[Disease Detection in Paddy Crop using CNN](https://sharathnpayyadi.github.io/projects/bachelor_thesis.html)** (Bachelor's thesis): CNN-based leaf image classification, published in IJRTE.

#### More robotics repositories
- **[panda_ws](https://github.com/SHARATHNPAYYADI/panda_ws)**: workspace to bring up the Franka Emika Panda arm and run manipulation scenarios.
- **[diff_drive_ws](https://github.com/SHARATHNPAYYADI/diff_drive_ws)**: differential-drive robot setup with localization.

### Embedded Systems

- **[Atmega-328p-WS](https://github.com/SHARATHNPAYYADI/Atmega-328p-WS)**: ATmega328P microcontroller programming workspace, built with Makefiles.

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

**DevOps & Tools**<br>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

## Education

- **M.Sc. Electrical and Information Technology**, Hochschule Darmstadt, Germany (2020 – 2022)
- **B.E. Electronics and Communication Engineering**, Visvesvaraya Technological University, India (2016 – 2020)

## Publications & Writing

- [Disease Detection in Paddy Crop using CNN Algorithm](https://www.ijrte.org/portfolio-item/f9835038620/), *International Journal of Recent Technology and Engineering (IJRTE)*, 2020
- [Why Simulation Is Essential in Robotics: A Beginner-Friendly Guide](https://medium.com/@sharathnp1998/why-simulation-is-essential-in-robotics-a-beginner-friendly-guide-0f48ba8eb664), Medium, 2026
- [How to Get Started With Robotics Simulation](https://medium.com/@sharathnp1998/how-to-get-started-with-robotics-simulation-6a5a0c2ec4da), Medium, 2026
- [Common Mistakes Beginners Make in Robotics Simulation](https://medium.com/@sharathnp1998/common-mistakes-beginners-make-in-robotics-simulation-edff0ac04958), Medium, 2026

More articles on [Medium](https://medium.com/@sharathnpayyadi).

---

<div align="center">

**Open to collaboration on autonomous systems, sim-to-real and multi-robot robotics.**<br>
Reach me at [sharathnpayyadi@gmail.com](mailto:sharathnpayyadi@gmail.com) or on [LinkedIn](https://www.linkedin.com/in/sharath-n-payyadi/).

</div>
