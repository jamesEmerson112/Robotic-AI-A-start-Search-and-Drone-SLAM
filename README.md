Project Documentation (README Example)

Project Name: Drone SLAM

Technologies: Python, (Robot Operating System), Pygame

Objective:

This project aims to implement a basic Simultaneous Localization and Mapping (SLAM) algorithm using OnlineGraph for a drone navigating from one location to another in an unknown 2D environment with randomly sized, spawn trees. The drone will use its sensor data, which only contains landmarks ID and their bearings with distances, to map the environment while simultaneously determining its own location in the map.

Demo:

Key Features:
	1.	SLAM Simulation: The drone will use sensor data to create a map and update its location in real-time.
	2.	Mapping Obstacles: The drone detects obstacles in its environment and maps them accordingly.
	3.	Path Planning: After building a basic map of the environment, the drone can plan paths around obstacles to reach specific targets.
	4.	Real-Time Update: The map and drone’s location are updated in real-time as the drone moves through the grid.

Technical Details:
	•	SLAM Algorithm: Implemented OnlineSLAM (because it's more efficient than GraphSLAM due to unknown large numbers of contraints) to estimate both the drone’s trajectory and the map simultaneously.
	•	Mapping: The SLAM algorithm is used to generate a map based on the drone’s movement and the detected obstacles.

Challenges and Solutions:
	•	Sensor Noise: Dealing with noisy sensor data was a major challenge. This was solved by applying filtering techniques (like Kalman Filters) to improve the accuracy of localization and mapping.
	•	Real-Time Performance: Ensuring real-time performance for both SLAM calculations and visualization in Pygame required optimization in data handling and computation.

---------------------------------------

Project Name: A* Search Algorithm

Technologies: Python, Pygame (for visualization)

Objective:

To implement the A search algorithm* to find the shortest path between a starting point and a goal on a 2D grid and a 2D grid with elevations. The project will visualize the algorithm’s behavior, showing how the search evolves and how nodes are explored and added to the path.

Demo:

Key Features:
	1.	Pathfinding Visualization: Uses Pygame to visualize the algorithm’s progress in finding the shortest path.
	2.	Heuristic Functions: Implements different heuristics for the search (Manhattan, Euclidean).
	3.	Dynamic Obstacles: Obstacles are added dynamically to the grid during the search, showing how the algorithm adapts to changes in real-time.

Technical Details:
	•	Algorithm: Implemented A* search with both Manhattan and Euclidean distance heuristics.

Challenges and Solutions:
	•	Handling Obstacles: Managing how obstacles affect the pathfinding process in real-time required constant recalculations, which were solved by updating the grid dynamically during the search.
	•	Heuristic Choice: Choosing the appropriate heuristic for different scenarios and optimizing it for efficiency in larger grids.
