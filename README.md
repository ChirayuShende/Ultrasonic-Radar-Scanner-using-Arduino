# Ultrasonic Radar Scanner using Arduino

An **Arduino-based radar system** that sweeps an ultrasonic sensor using a servo motor to detect objects and stream distance measurements in real time via serial communication.

The system mimics a basic radar by rotating the ultrasonic sensor across an angle range and measuring distances at each step. The collected data can be visualized on a computer using a serial plotter or custom visualization software.

---

## Project Overview

This project uses:

- Arduino board  
- HC-SR04 Ultrasonic Sensor  
- Servo Motor  
- Serial Communication  

The servo motor rotates the ultrasonic sensor between **15° and 165°**, scanning the surrounding area. At each position, the sensor measures the distance to nearby objects and sends the angle-distance data through the serial port.

The output format sent to the serial monitor:

angle,distance.

Example output:

90,35.  
91,36.  
92,34.  

Where:
- **angle** → servo position in degrees  
- **distance** → measured distance in centimeters  

---

# Features

- Real-time object detection  
- Radar-style scanning using a servo motor  
- Serial data streaming for visualization  
- Simple and low-cost hardware setup  
- Easy to extend with graphical radar displays  

---

# Hardware Requirements

| Component | Quantity |
|-----------|----------|
| Arduino Uno (or compatible board) | 1 |
| HC-SR04 Ultrasonic Sensor | 1 |
| Servo Motor (SG90 recommended) | 1 |
| Jumper Wires | Several |
| Breadboard (optional) | 1 |

---

# Pin Configuration

| Component | Arduino Pin |
|----------|-------------|
| Ultrasonic Trigger | 10 |
| Ultrasonic Echo | 11 |
| Servo Signal | 12 |

---

# Circuit Diagram (Connections)

### HC-SR04 Ultrasonic Sensor

| Sensor Pin | Arduino |
|-------------|--------|
| VCC | 5V |
| GND | GND |
| Trig | Pin 10 |
| Echo | Pin 11 |

### Servo Motor

| Servo Wire | Arduino |
|------------|--------|
| Red | 5V |
| Brown/Black | GND |
| Yellow/Orange | Pin 12 |

---

# How It Works

1. The servo motor rotates the ultrasonic sensor from **15° to 165°**.
2. At each angle, the Arduino triggers the ultrasonic sensor.
3. The sensor sends a sound pulse and waits for the echo.
4. The Arduino calculates the distance based on the time taken for the echo to return.
5. The angle and distance are transmitted via serial communication.

---

# Running the Project

1. Connect the hardware according to the wiring table.
2. Upload the Arduino sketch to your board using the Arduino IDE.
3. Open the Serial Monitor or Serial Plotter.
4. Set the baud rate to **9600**.
5. Observe the streamed radar data.

---

# Possible Improvements

- Add Processing or Python radar visualization  
- Implement object tracking  
- Increase scan range to **0–180°**  
- Add multiple sensors for better coverage  
- Integrate with robotic navigation systems  

---

# Applications

- Basic radar simulation  
- Obstacle detection  
- Robotics projects  
- Smart surveillance systems  
- STEM learning and educational demonstrations  

