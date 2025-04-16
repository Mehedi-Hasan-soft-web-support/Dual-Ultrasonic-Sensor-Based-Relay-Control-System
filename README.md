# Dual-Ultrasonic-Sensor-Based-Relay-Control-System

# Dual Ultrasonic Sensor-Based Relay Control System

This Arduino project uses two ultrasonic sensors to control a relay module based on object detection. It can be used for automation tasks like triggering a device when someone approaches and turning it off when they leave from another direction.

## 🛠️ Hardware Components

- Arduino Uno (or compatible board)
- 2 × HC-SR04 Ultrasonic Sensors
- 1 × Relay Module
- Jumper wires
- Power supply

## 🔌 Pin Configuration
_____________________________________
| Component           | Arduino Pin |
|----------------     |-------------|
| Sensor 1 Echo       | A0          |
| Sensor 1 Trigger    | A1          |
| Sensor 2 Echo       | A2          |
| Sensor 2 Trigger    | A3          |
| Relay Module        | Digital 8   |
_____________________________________

## 📏 Detection Logic

- **THRESHOLD:** 15 cm
- **Sensor 1 detection:** Turns **ON** the relay.
- **Sensor 2 detection:** Turns **OFF** the relay.
- This mimics entering and exiting a space, making it ideal for door-based automation or corridor lights.

## 🧠 Code Overview

- `checkSensor()` measures the distance using each ultrasonic sensor.
- Relay state is tracked with a boolean `relayState`.
- The relay state is updated in real time based on the sensor readings.

## 💡 Example Use Case

Imagine a hallway or entry system where:
- A person enters → Sensor 1 detects them → Relay turns ON (e.g., turns on a light).
- The person exits → Sensor 2 detects them → Relay turns OFF.

## 🧾 License

This project is open-source and available under the MIT License.

---

### 📷 Future Improvements
- Add an LCD or OLED display for distance readout.
- Add a timer to delay the relay turning off.
- Integrate with IoT platforms for remote monitoring.

