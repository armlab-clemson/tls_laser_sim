# TLS Laser Sim

Version 1 of the simulation of a VLP-16 Lidar on a floating 6DOF frame observing measurements of 3 distinct objects. 

<img src="./images/laser_v1.gif" style="zoom: 67%;" />

**Dependencies:**

- [velodyne_simulator package](https://github.com/ToyotaResearchInstitute/velodyne_simulator.git) 
- Gazebo

**Note**: Tested on ROS Melodic



**Implementation:**

The Lidar pose is controlled with `geometry_msgs/Twist` by publishing to `/cmd_vel`

Launch simulation:

```bash
$ roslaunch sim_description sim.launch
```

Keyboard Teleop:

```bash
$ rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```



**To Do:**

- [x] Adding `/odom` functionality to the 6DOF plugin for ground truth of Lidar pose
- [ ] Adding `/odom_cov` or `/imu` functionality to the plugin for realistic noisy measurements of Lidar pose
- [ ] Adding rudimentary feature detection to extract sensor measurements that correspond to features (here, spheres)

