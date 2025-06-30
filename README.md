# 🚀 Robotics & Pathfinding Simulations

![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

A collection of interactive simulations and algorithms for robotics and pathfinding, with real-time visualizations.

---

## Table of Contents
- [Particle Filter Spaceship Localization](#particle-filter-spaceship-localization)
- [Drone SLAM](#drone-slam)
- [A* Search Algorithm](#a-search-algorithm)
- [Getting Started](#getting-started)
- [Contact](#contact)

---

## Particle Filter Spaceship Localization

![Spaceship Demo](assets/proj1.gif)

**Technologies:** Python, Pygame (for visualization)

**Objective:**  
This project implements a particle filter algorithm to localize a simulated spaceship navigating the solar system. The simulation features a sun, the Earth in orbit, and, on harder levels, additional planets. The spaceship must determine its position using only gravity measurements and steering angles. Once localized, the simulated spaceship sends messages back to Earth.

**Key Features:**
- **Particle Filter Localization:** Uses a particle filter to estimate the spaceship’s position based on noisy gravity and steering data.
- **Solar System Simulation:** Models the sun, Earth, and (optionally) other planets, providing a dynamic environment for localization.
- **Difficulty Levels:** Harder levels introduce more planets, increasing the complexity of the localization problem.
- **Communication Simulation:** After successful localization, the spaceship simulates sending messages back to Earth.

**Technical Details:**
- The particle filter algorithm handles uncertainty in sensor data (gravity, steering).
- The simulation tests the algorithm’s robustness in increasingly complex planetary systems.

**Challenges and Solutions:**
- **Sensor Uncertainty:** The algorithm must accurately localize the spaceship with only indirect measurements (gravity, steering).
- **Scalability:** The system is designed to handle additional planets and increased complexity.
- **Validation:** All tests for the project have been passed, indicating correctness and robustness.

---

## Drone SLAM

![Drone SLAM Demo](assets/proj2.gif)

**Technologies:** Python, (Robot Operating System), Pygame

**Objective:**  
This project aims to implement a basic Simultaneous Localization and Mapping (SLAM) algorithm using OnlineGraph for a drone navigating from one location to another in an unknown 2D environment with randomly sized, spawn trees. The drone will use its sensor data, which only contains landmarks ID and their bearings with distances, to map the environment while simultaneously determining its own location in the map.

**Demo:** Please reach out for a presentation and a demo.

**Key Features:**
- **SLAM Simulation:** The drone will use sensor data to create a map and update its location in real-time.
- **Mapping Obstacles:** The drone detects obstacles in its environment and maps them accordingly.
- **Path Planning:** After building a basic map of the environment, the drone can plan paths around obstacles to reach specific targets.
- **Real-Time Update:** The map and drone’s location are updated in real-time as the drone moves through the grid.

**Technical Details:**
- **SLAM Algorithm:** Implemented OnlineSLAM (more efficient than GraphSLAM due to unknown large numbers of constraints) to estimate both the drone’s trajectory and the map simultaneously.
- **Mapping:** The SLAM algorithm is used to generate a map based on the drone’s movement and the detected obstacles.

**Challenges and Solutions:**
- **Sensor Noise:** Dealing with noisy sensor data was a major challenge. This was solved by applying filtering techniques (like Kalman Filters) to improve the accuracy of localization and mapping.
- **Real-Time Performance:** Ensuring real-time performance for both SLAM calculations and visualization in Pygame required optimization in data handling and computation.

---

## A* Search Algorithm

**Technologies:** Python, Pygame (for visualization)

**Objective:**  
To implement the A* search algorithm to find the shortest path between a starting point and a goal on a 2D grid and a 2D grid with elevations. The project will visualize the algorithm’s behavior, showing how the search evolves and how nodes are explored and added to the path.

**Demo:** Please reach out for a presentation and a demo.

**Key Features:**
- **Pathfinding Visualization:** Uses Pygame to visualize the algorithm’s progress in finding the shortest path.
- **Heuristic Functions:** Implements different heuristics for the search (Manhattan, Euclidean).
- **Dynamic Obstacles:** Obstacles are added dynamically to the grid during the search, showing how the algorithm adapts to changes in real-time.

**Technical Details:**
- **Algorithm:** Implemented A* search with both Manhattan and Euclidean distance heuristics.

**Challenges and Solutions:**
- **Handling Obstacles:** Managing how obstacles affect the pathfinding process in real-time required constant recalculations, which were solved by updating the grid dynamically during the search.
- **Heuristic Choice:** Choosing the appropriate heuristic for different scenarios and optimizing it for efficiency in larger grids.

---

## Getting Started

```bash
# Example: Run the A* visualizer
python astar/main.py
```
*Update with actual run instructions for each project as needed.*

---

## Contact

For demos or questions, reach out via [your email/contact info].
