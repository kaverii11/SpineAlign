# SpineAlign
POSTURE CORRECTION DEVICE USING SENSORS
Body Posture Detection with IMU, Flex, and Ultrasonic Sensors

Overview

This project utilizes multiple sensors to detect body posture accurately. The system integrates an MPU6050 IMU sensor, flex sensors, and an ultrasonic distance sensor to analyze movement and position. Data is processed using Arduino.

Features

Real-time posture tracking using accelerometer, gyroscope, and flex sensor data.
.

Sensor fusion using MPU6050's Digital Motion Processing (DMP).

Ultrasonic distance measurement for position detection.

Posture classification based on sensor data.

Hardware Requirements

MPU6050 (6-axis accelerometer + gyroscope sensor)

Flex sensors (to detect joint bending)

Ultrasonic distance sensor (e.g., HC-SR04 for measuring proximity)

Arduino Uno/Nano/ESP32 (or any compatible microcontroller)

USB cable for serial communication

Jumper wires

Software Requirements

Arduino IDE

Install the MPU6050 library by Electronic Cats
Sketch -> Include Library -> Manage Libraries -> Search "MPU6050" -> Install
Install I2Cdev library (required for MPU6050 communication).
Install NewPing library for the ultrasonic sensor.


Setup & Installation

Connect MPU6050 to Arduino:
VCC  -> 3.3V / 5V (depending on board)
GND  -> GND
SDA  -> A4 (on Uno) / D21 (on ESP32)
SCL  -> A5 (on Uno) / D22 (on ESP32)
Connect Flex Sensors to Arduino:

One end of the flex sensor goes to VCC (5V).

The other end is connected to an analog input (A0) via a pull-down resistor.

Connect Ultrasonic Sensor (HC-SR04):
VCC   -> 5V
GND   -> GND
Trig  -> D9
Echo  -> D10

Upload Arduino Code:

Open the Arduino sketch (posture_detection.ino).

Select the correct board and port.

Upload the code.

Run Processing Visualization:

Open posture_visualization.pde in Processing.

Modify COMXX in setup() to match your Arduino's serial port.

Run the Processing sketch to visualize posture in real time.

Author

Developed by Kaveri Sharma, Khushi B, and Khushi Mahesh.
