# IMU-Calibration

To create test data, IMU was positioned in the way, that one of its axes was aligned with gravity. Then IMU acceleration and angular rate were recorded of this axis approx. 1 min.
This allows for averaging the acceleration and angular rate over time. Then IMU was turned upside down to achieve gravity in the opposite direction. Process was repeated for all 3 axis. 
This produces bias and scale factor error to timeseries, that following process calculates.
