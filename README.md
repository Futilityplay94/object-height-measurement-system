# 📏 Object Height Measurement System

An automated, non-contact height measurement system built with **Arduino Uno**, **HC-SR04 Ultrasonic Sensor**, **SG90 Servo Motor**, and an **OLED Display**.

---

## 🔍 Overview

This project measures the height of static objects using ultrasonic echo-ranging. The sensor is mounted at a fixed height (30 cm), and the object's height is calculated by subtracting the measured distance from that reference. Results are shown in real time on an OLED display, and a servo motor reacts by rotating to an angle corresponding to the measured height.

---

## ⚙️ Components

| Component                  | Quantity |
|---------------------------|----------|
| Arduino Uno               | 1        |
| Ultrasonic Sensor HC-SR04 | 1        |
| Servo Motor SG90          | 1        |
| OLED Display (0.96" I2C)  | 1        |
| Breadboard                | 1        |
| Jumper Wires              | As needed |
| USB Cable / Power Supply  | 1        |

---

## 🔌 Circuit Connections

### HC-SR04 Ultrasonic Sensor
| Sensor Pin | Arduino Pin |
|-----------|-------------|
| VCC       | 5V          |
| GND       | GND         |
| TRIG      | Pin 9       |
| ECHO      | Pin 10      |

### OLED Display (I2C SSD1306)
| Display Pin | Arduino Pin |
|------------|-------------|
| VCC        | 5V          |
| GND        | GND         |
| SDA        | A4          |
| SCL        | A5          |

### Servo Motor SG90
| Servo Wire       | Arduino Pin |
|-----------------|-------------|
| Red (VCC)       | 5V          |
| Black/Brown (GND) | GND       |
| Yellow/Orange (Signal) | Pin 6 |

---

## 🧠 Working Principle

1. **Ultrasonic Sensor** emits a 40 kHz pulse and measures the echo return time.
2. **Distance** is calculated as: `Distance = (Time × 0.0343) / 2` (in cm)
3. **Object Height** = `Sensor Height (30 cm) − Measured Distance`
4. The **OLED Display** shows the height in real time.
5. The **Servo Motor** rotates to a specific angle based on height:

| Object Height | Servo Angle |
|--------------|-------------|
| < 10 cm      | 0°          |
| 10–14 cm     | 45°         |
| 14–18 cm     | 90°         |
| 18–24 cm     | 135°        |
| ≥ 24 cm      | 180°        |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/object-height-measurement.git
cd object-height-measurement
```

### 2. Install Required Libraries

In the Arduino IDE, go to **Sketch → Include Library → Manage Libraries** and install:

- `Adafruit SSD1306`
- `Adafruit GFX Library`
- `Servo` *(built-in, no installation needed)*

### 3. Upload the Code

1. Open `src/height_measurement.ino` in Arduino IDE.
2. Select **Board:** Arduino Uno and the correct **Port**.
3. Click **Upload**.

### 4. Open Serial Monitor

Set baud rate to `9600` to view live height readings in the Serial Monitor.

---

## 📁 Project Structure

```
object-height-measurement/
│
├── src/
│   └── height_measurement.ino   # Main Arduino sketch
│
├── docs/
│   └── project_report.md        # Full project report
│
├── diagrams/
│   └── circuit_description.md   # Pin connection reference
│
├── README.md                    # This file
└── LICENSE                      # MIT License
```

---

## ✅ Applications

- 📦 Logistics & parcel dimension measurement
- 🏭 Assembly line product inspection
- 🌱 Greenhouse plant growth monitoring
- 🤖 Robotics object detection
- 🎓 Embedded systems education

---

## ⚠️ Limitations

- Soft or angled surfaces may cause inconsistent ultrasonic readings.
- Environmental factors (temperature, humidity) can affect accuracy.
- Fixed sensor height limits the range to objects shorter than 30 cm.

---

## 🔭 Future Scope

- Add **Wi-Fi/Bluetooth** for remote monitoring
- Use **multiple sensors** for 3D profiling (width + depth)
- Integrate **SD card** or **cloud storage** for data logging
- Add **computer vision** for intelligent object profiling

---

## 📚 References

- [Arduino Documentation](https://www.arduino.cc/)
- [HC-SR04 Sensor Guide](https://www.electronicwings.com/)
- [Adafruit SSD1306 OLED Guide](https://learn.adafruit.com/monochrome-oled-breakouts)
- [Servo Motor with Arduino](https://lastminuteengineers.com/servo-motor-arduino-tutorial/)

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.
