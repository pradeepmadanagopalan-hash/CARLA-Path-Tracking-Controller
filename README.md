⭐ **1. Introduction**

Modern autonomous driving systems require robust trajectory tracking and control to follow planned routes accurately in simulation environments like CARLA.

This project implements an end-to-end waypoint tracking controller that enables a simulated vehicle to follow a predefined path using classical control methods. It combines longitudinal speed control and lateral steering control into a unified closed-loop system.

🎥 Simulation Environment Demo - Race Track

<table>
  <tr>
    <td align="center">
      <b>Main Straight </b><br>
      <img src="Images/Longitudinal_Tracking.gif" width="400"/>
    </td>
    <td align="center">
      <b>Corners </b><br>
      <img src="Images/Lateral_Tracking.gif" width="400"/>
    </td>
  </tr>
</table>

---

🧩 **2. Challenge**

This project addresses the challenges of real-time trajectory tracking and vehicle control in a simulated autonomous driving environment using CARLA.

The vehicle is evaluated on a predefined test track represented as a sorted sequence of waypoints. These waypoints are uniformly spaced along the track and serve as the reference trajectory for the controller. Each waypoint contains both position (x, y) and target speed, meaning the reference signal defines both where the vehicle should go and how fast it should travel.

Key challenges include:

- Maintaining stable path tracking under continuously changing vehicle states (speed, yaw, position).  
- Handling discretized waypoint inputs that introduce noise and discontinuities in the reference trajectory.  
- Balancing longitudinal speed control with lateral steering control in a closed-loop system.  
- Ensuring numerical stability in PID control and robustness of steering at low speeds.

<p align="center">
  <img src="Images/Test_Track.png" width="400"/>
</p>
  
---

🎯 **3. Objectives**

This project focuses on building a robust waypoint tracking controller for autonomous vehicle simulation in CARLA.

Key objectives include:

- Develop a longitudinal control system for accurate speed tracking using PID control.  
- Design a lateral control system for stable path following using Stanley steering control.  
- Enable simultaneous position and velocity tracking using a unified closed-loop controller.  
- Convert reference waypoints into actionable vehicle commands (throttle, brake, steering).  

---

