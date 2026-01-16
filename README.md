# 🧍‍♂️ SpineAlign  
## Posture Correction Device Using Sensors

**SpineAlign** is a smart posture monitoring system that uses sensor fusion to detect incorrect body posture in real time. By combining IMU, flex, and ultrasonic sensors, the device accurately tracks body alignment and helps classify posture based on movement and position data.

---

## 📌 Overview

SpineAlign leverages multiple sensors to analyze body orientation, joint bending, and distance from reference points. The system processes sensor data using an Arduino-compatible microcontroller and visualizes posture in real time using **Processing**.

**Sensors Used:**
- MPU6050 – Accelerometer + Gyroscope (IMU)
- Flex Sensors – Detect joint bending
- Ultrasonic Sensor (HC-SR04) – Measures proximity and position

---

## ✨ Features

- Real-time posture tracking  
- Sensor fusion using MPU6050 Digital Motion Processing (DMP)  
- Detection of body inclination and joint bending  
- Ultrasonic-based distance measurement  
- Posture classification using combined sensor data  
- Live posture visualization using Processing  

---

## 🛠 Hardware Requirements

- MPU6050 (6-axis accelerometer + gyroscope)
- Flex sensors
- Ultrasonic distance sensor (HC-SR04)
- Arduino Uno / Nano / ESP32 (or compatible)
- USB cable
- Jumper wires
- Pull-down resistors (for flex sensors)

---

## 💻 Software Requirements

- Arduino IDE
- Processing IDE

### Required Arduino Libraries

Install the following libraries from **Arduino Library Manager**:

- MPU6050 by Electronic Cats  
- I2Cdev (dependency for MPU6050)  
- NewPing (for ultrasonic sensor)

---

## 🔌 Circuit Connections

### MPU6050 → Arduino

| MPU6050 | Arduino Uno | ESP32 |
|------|------------|-------|
| VCC | 3.3V / 5V | 3.3V |
| GND | GND | GND |
| SDA | A4 | D21 |
| SCL | A5 | D22 |

---

### Flex Sensor → Arduino

- One end → **5V**
- Other end → **Analog Pin (A0)**
- Use a **pull-down resistor** to GND

---

### Ultrasonic Sensor (HC-SR04) → Arduino

| HC-SR04 | Arduino |
|-------|--------|
| VCC | 5V |
| GND | GND |
| Trig | D9 |
| Echo | D10 |

---

## 🚀 Setup & Installation

### 1️⃣ Upload Arduino Code

1. Open `posture_detection.ino`
2. Select the correct **board** and **COM port**
3. Upload the sketch to the Arduino

---

### 2️⃣ Run Visualization

1. Open `posture_visualization.pde` in **Processing**
2. Update the serial port inside `setup()`:
   ```java
   new Serial(this, "COMXX", 9600);
3. Run the sketch to visualize posture data in real time

### 📊 How It Works

MPU6050 tracks orientation and motion

Flex sensors detect joint bending

Ultrasonic sensor measures distance from reference

Sensor data is fused and processed on Arduino

Posture is classified and visualized live

### 👩‍💻 Authors

Kaveri Sharma

Khushi B

Khushi Mahesh
