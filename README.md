# Assessment of UR10e Force Control
Test setup and test scenarios for the comparison/assessment of UR10e force control.

This repository also contains the data of the
* accepted open-access journal paper (Mechanical Sciences, Advances in Service and Industrial Robotics – RAAD2021)\
Gadringer S., Gattringer H., Mueller A.,  Assessment of force control for surface finishing – An experimental comparison between Universal Robots UR10e and FerRobotics active contact flange, *Mechanical Sciences*, 2022.
* published conference paper (RAAD 2021)\
Gadringer S., Gattringer H., Mueller A., Assessment of Universal Robot Force Control and External Force Compliance Device for Surface Treatment, *30th International Conference on Robotics in Alpe-Adria-Danube Region (RAAD)*, Springer, https://doi.org/10.1007/978-3-030-75259-0_9, 2021.

## General Information UR10e/ACF Comparison

* Depending on the test case (ACF or UR force control mode), the UR either uses position or force control to follow the desired TCP path. For the upwards movement at the end of the test case, the UR always operates in position control mode.
* The velocities of ACF and UR force control vary highly due to the differences of UR position and force control. So the UR might be delayed at first contact with a work piece and requires synchronization for a direct comparison between UR and ACF. Time t=0 determines the start of the contact.

## Test Scenarios

### Ramp Profile


At the beginning, the UR waits at start pose p_s before it vertically moves downwards until reaches contact with the work piece at pose p_sc . There it stays constant for a time of 4s to allow settling of the force. Afterwards, the UR continues the movement along the contour until it reaches pose p_ec. After a 2s long stop, the robot moves vertically upwards to the end pose p_e using position control, independent of the test case.

### Straight Profile

At the beginning, the UR waits at start pose p_s before it vertically moves downwards until reaches contact with the work piece at pose p_sc . There it stays constant for a time of 4s to allow settling of the force. Afterwards, the UR continues the the horizontal movement until it reaches pose p_ec. After a 2s long stop, the robot moves vertically upwards to the end pose p_e using position control, independent of the test case.

### Direct Sensor Contact

The desired robot path is simply a vertical movement from start pose p_s to contact pose p_c. There the robot stands still for six seconds before it moves back to start or rather end pose p_e.
