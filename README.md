# RobotCat
Shapes and Links for RL Robot Cat


Link to Waveshare board:
https://www.waveshare.com/wiki/General_Driver_for_Robots

Drivers: 
"ESP32Servo" for ESP32. https://madhephaestus.github.io/ESP32Servo/annotated.html
"INA219_WE" https://github.com/wollewald/INA219_WE


I2C Addresses:
I2C device found at address 0x0C - AK09918_I2C_ADDR (3-axis Electronic Compas) \
I2C device found at address 0x42 - INA219_I2C_ADDR (output current/voltage/power monitor) \
I2C device found at address 0x6B - QMI8658_I2C_ADDR (IMU) \
I2C device found at address 0x77 - BMP280_I2C_ADDR (Temp Sensor) \
I2C device found at address 0x7E - 

IMU and Compass, use IMU, AK09918, and QMI8658 from Waveshare:
```
  imuDataGet( &stAngles, &stGyroRawData, &stAccelRawData, &stMagnRawData);
  IMU_Temp = QMI8658_readTemp();
  GyroX_New = stGyroRawData.s16X;
  Compass_X = stMagnRawData.s16X;
  Angles_Data_Z = stAngles.s16X;
  AccelRa_Data_X = stAccelRawData.s16X
```

// Recommended PWM GPIO pins on the ESP32 include 2,4,12-19,21-23,25-27,32-33 


https://github.com/PetoiCamp/OpenCat
