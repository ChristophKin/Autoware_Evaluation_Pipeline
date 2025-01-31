# Autoware_Evaluation_Pipeline
Python evaluation pipeline for evaluation of localisation and drive/gait of vehicles/quadrupeds in Autoware.

- statistic analysis of the gait/drive with IMU and Twist data
- localization analysis with NDT and EKF performance parameter
- for Simulation only: localization evaluation with ground truth data from the Simulator (e.g. Isaac Sim)
- creation of correlation matrices, evaluation tables and other plots for visualization
- option for zero-phase-filtering all input data

The following topics need to be in the rosbag:
- /diagnostics (for Mahalanobis distance evaluation, the value needs to be added in the autoware code to the diagnostics topic)
- IMU: /sensing/imu/imu_data
- Twist: /sensing/vehicle_velocity_converter/twist_with_covariance
- TF: /tf (for estimation error, ground truth and estimated pose tf need to be recorded)

![IMU and Twist](https://github.com/user-attachments/assets/383c0410-723e-4a9f-983e-0701257341ad)

<img src="https://github.com/user-attachments/assets/00600ba4-0268-46e4-8fc7-135e5319ff3b" width="300">

![estimation Error_page-0001](https://github.com/user-attachments/assets/3dbf4847-f15c-4a75-b80c-2bba31799d8b)

<img src="https://github.com/user-attachments/assets/2b5cabae-c04b-4ca5-b088-b454606ce610" width="800">

<img src="https://github.com/user-attachments/assets/7b74467f-9e64-4fc1-b67a-b0b2644fc220" width="600">

<img src="https://github.com/user-attachments/assets/cb2f9543-5e41-4bd7-b573-79bae884d938" width="600">

![correlationMatrix_rosbag2_2024_12_03-10_34_42_absolut_velocity_vs_ekf_page-0001](https://github.com/user-attachments/assets/5993ad32-f9f2-40bf-87e3-b1928dc0ec54)
