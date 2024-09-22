# AeroVision: Intelligent Drone Surveillance

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

## Installation Process

In the GitHub repository, you will find two zip files: `SinAssets.zip` and `SoloAssets.zip`. The project file was too large, so we had to split it into two parts. `SinAssets.zip` contains all the Unity files and configurations. `SoloAssets.zip` contains the Unity project's Assets folder, including scripts, models, textures, etc. Download both zip files and extract them. Move the Assets folder from `SoloAssets.zip` into the extracted folder from `SinAssets.zip` to have the full project in one place.

### Running the Project

To run the project, follow these steps:

1. First, run the `deteccion_camara.py` file and wait for it to print a message indicating that it's waiting for a connection.
2. Next, run the `agents.py` file and wait for it to print a message saying it's waiting for a connection. Note that you will need to rerun `agents.py` each time you close Unity, as closing the game will also stop this script. However, `deteccion_camara.py` will continue running even if you close Unity.
3. Each script should be run in its own terminal.

### Unity Setup

For the Unity project, you need to assign several references in the Inspector:

- In the `dron_agent.cs` script:
  - The points of interest are the spheres at the doors.
  - The spawn guard points are the spheres at the vault.
  - The zones are spheres located below the floor at the doors.

- In the `dron_deteccion.cs` script:
  - You need to assign the cameras.

Some scripts use tag references instead of Inspector references, so you will need to ensure the appropriate tags are added.

Make sure that both the Unity and Python scripts have the same server and IP settings for the detection and agent systems.

### Additional Information

- `Camara_stream.cs` and `captura_imagenes.cs` were only used to take screenshots of the game for training the YOLO model.
  
- For the computer vision part, in a separate Python window, run the `4_yolo_opencv_detector` script. Verify that the Unity editor window name matches the one specified in the script. Also, check that the paths to the `.weights` and `.cfg` files are correct. You will find one of each in the `yolo_opencv_detector` folder and another set in the same folder as the `4_yolo_opencv_detector` script. These are duplicates, so you can use either set to run the model.

Additional Jupyter notebooks are included to help you train your own YOLO model if needed. The guide for this can be found at the following link:

[How to Train a YOLOv4 Model](https://www.youtube.com/watch?v=RSXgyDf2ALo)

[Project video link](https://youtu.be/FohCQ_peNsw)
