
# Smart Parking System with I2C LCD Scanner using Arduino

This project implements a Smart Parking System using Arduino Uno, IR sensors, a servo motor, and an I2C LCD display. It also includes an I2C scanner code to detect the LCD's address on the I2C bus.

## Project Overview

This system automates the parking process by detecting vehicle entry and exit using IR sensors. It opens or closes a gate with a servo motor based on parking slot availability. The remaining slots are displayed on an I2C LCD, making it easy to monitor in real-time.

### Project Image:
![Smart Parking System](path/to/your/project-image.jpg)



## Features
- Automated gate control using IR sensors and a servo motor.
- Parking slot availability monitoring and display on an LCD screen.
- An I2C scanner to detect and configure the LCD display.
- Simple and expandable design for larger parking lots.

## Components Required
1. **Arduino Uno** – The microcontroller used to control the system.
2. **IR Sensors (2)** – Used to detect vehicle entry and exit.
3. **Servo Motor** – Controls the gate for entry and exit.
4. **16x2 LCD Display (I2C)** – Displays the number of parking slots left and status messages.
5. **LED** – Used as an indicator for system status.
6. **Breadboard** – For building the circuit.
7. **Jumper Wires** – To connect all the components.
8. **Power Source** – Can be a 5V USB or external power supply.

## Setup and Connections
- **IR1 Sensor** (Pin 2) – Detects vehicle entry.
- **IR2 Sensor** (Pin 4) – Detects vehicle exit.
- **Servo Motor** (Pin 3) – Controls gate mechanism.
- **LED** – Can be connected to any available digital pin and ground for system status indication.
- **LCD I2C Display** – Connected to the SDA (Pin A4) and SCL (Pin A5) of the Arduino.
  
**Power:** Connect the Arduino to a 5V power source or USB.

## How to Use
1. **Assemble the Components** – Connect all components according to the setup.
2. **Upload the I2C Scanner Code** – Use the provided I2C scanner code to detect the I2C address of your LCD.
3. **Update the Address in the Main Code** – Modify the `LiquidCrystal_I2C lcd(0x27,16,2);` line with the detected address if different.
4. **Upload the Parking System Code** – After confirming the LCD address, upload the main parking system code.
5. **Monitor the Parking System** – The LCD will display messages, and the gate will open and close based on parking availability.

## Future Improvements
- Add a display for the total number of parking slots on startup.
- Implement RFID-based access for secure parking management.
- Add a web or mobile interface for real-time monitoring.
