# AeroVision: Intelligent Drone Surveillance

**Date:** August 2024 - September 2024  
**Technologies:** Unity, C#, Python, YOLOv4, WebSockets

## Overview
AeroVision is a cutting-edge 3D surveillance system designed using Unity, C#, and Python. The project simulates a construction site environment where drones and security cameras detect intruders and relay the information to security guards. This system employs AI-powered agents to intelligently manage real-time monitoring, enhancing both the gameplay dynamics and security protocols.

## Features
- **Immersive 3D Environment:**  
  Built a detailed construction site in Unity where drones monitor the area from above and ground cameras survey different zones.

- **Intelligent Agent System:**  
  Implemented Python-based agents capable of intelligent decision-making. These agents communicate with Unity in real-time using WebSocket protocols, allowing for efficient task execution and coordination.

- **YOLOv4 Integration for Object Detection:**  
  Trained a custom YOLOv4 model for computer vision within the game, achieving an 88% accuracy rate. The model detects and classifies objects such as construction equipment, workers, and intruders (thieves) in real time.

- **Real-Time Surveillance System:**  
  The drones and cameras continuously monitor the environment for any intruders. When a threat is detected, it is immediately communicated to the security guard agent, who then takes appropriate action.

## Installation & Setup
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/AeroVision.git
   cd AeroVision
