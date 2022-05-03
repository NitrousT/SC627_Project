# Path Planning (Fu-astar)

---

The goals of this project are the following:

* Implement Trajectory modules for highway driving.
* Test implementation by driving a car on a highway (in a simulator), maintaining a speed close to 50 mph and safely changing lanes to go around slower traffic.

---

## 1. Files

My project includes the following files:

- [<b>README.md</b> - A summary of the project]
- [<b>Full_video.mp4</b> - Video showing the car driving on the highway for 10 miles without incidents]


## 2. Project Description
Felxible Unit-Astar, a theoretical Path Planning algorihtm was integrated with the Unity Simulator to show autonomous driving of a car on a highway.

In this project, a highway map is provided as waypoints. The highway is 6945.554m long and looks like this in global xy space:
<div style="text-align:center"><img src="https://github.com/ArjaanBuijk/CarND-Path-Planning-Project/blob/master/images/highway-map-xy.gif?raw=true" style="width:500px;"/></div>

The objective of our project is to write the <b>Trajectory</b> modules, and provide the simulator with a trajectory for the car to follow. The trajectory is defined by points along a path with a certain spacing. The spacing indicates the distance the car must drive in 0.02 seconds (simulator constraint) and thus defines the speed along the trajectory.

The simulator uses this trajectory and takes care of the <b>Motion Control</b>, so that the car indeed follows the trajectory at the defined speed.

The simulator also takes care of <b>Sensor Fusion</b> and <b>Localization</b>, and each cycle it provides the results back, so we can update the trajectory.

<b>Sensor Fusion data provided by simulator</b>

---

### Dependencies
* You can download the Term3 Simulator which contains the Path Planning Project from the releases tab (https://github.com/udacity/self-driving-car-sim/releases)
* Download the Unity Simulator to run the code.(original version: 5.5f1 Note: If you change the unity editor version you will have to manually upgrade the code)

* cmake >= 3.5
* make >= 4.1
* gcc/g++ >= 5.4
* [uWebSockets](https://github.com/uWebSockets/uWebSockets)
* Run ./install-ubuntu.sh to install necessary files [Only ubuntu]

## Basic Build Instruction

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./path_planning`.
