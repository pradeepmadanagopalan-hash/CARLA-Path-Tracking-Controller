This folder contains the core CARLA waypoint tracking and evaluation components, including the 2D vehicle controller, 
simulation execution script, utility helpers for persistent state management, and a grading module that validates trajectory and speed tracking performance against reference waypoints.

- **my_controller2d.py** implements the main 2D vehicle controller, using PID for speed tracking and a Stanley-inspired approach for steering based on waypoint following.
- **cutils.py** provides a lightweight utility class for storing persistent controller state variables across simulation frames.
- **module_7.py** runs the CARLA waypoint navigation demo, handling simulation setup, waypoint interpolation, live plotting, controller execution, and data logging.
- **grade_c1m7.py** evaluates controller performance by comparing the generated trajectory against ground-truth waypoints using distance and speed error thresholds.
- The **controller_output** folder stores simulation results generated during execution, including trajectory visualizations, control signal plots (throttle, steering, brake, and speed profiles), and logged vehicle state data
  (position, velocity, and timestamp) used for post-run analysis and performance evaluation.
