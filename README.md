# IMU-Calibration

To create test data, IMU was positioned in the way, that one of its axes was aligned with gravity. Then IMU acceleration and angular rate were recorded of this axis approx. 1 min.
This allows for averaging the acceleration and angular rate over time. Then IMU was turned upside down to achieve gravity in the opposite direction. Process was repeated for all 3 axis. 
This produces bias and scale factor error to timeseries, that following process calculates.

## For Accelometers

### Upward Force Measurement
$$ f_{up} = b_a + (1 + S_a)g $$

### Downward Force Measurement
$$ f_{down} = b_a - (1 + S_a)g $$

### Accelerometer Bias
$$ b_a = \frac{f_{up} + f_{down}}{2} $$

### Accelerometer Scale Factor
$$ S_a = \frac{f_{up} - f_{down} - 2g}{2g} $$

## For Angular Rates

### Upward Angular Rate Measurement
$$ \omega_{up} = b_g + (1 + S_g)\omega_e \sin \phi $$

### Downward Angular Rate Measurement
$$ \omega_{down} = b_g - (1 + S_g)\omega_e \sin \phi $$

### Gyroscope Bias
$$ b_g = \frac{\omega_{up} + \omega_{down}}{2} $$

### Gyroscope Scale Factor
$$ S_g = \frac{\omega_{up} - \omega_{down} - 2\omega_e \sin \phi}{2\omega_e \sin \phi} $$
