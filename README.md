# RC Electric Car Bot 🏎️🤖

A smart, remote-controlled (RC) electric car bot built using an microcontroller and motor drivers. This project allows you to control a hardware chassis wirelessly via Bluetooth/Wi-Fi or a custom controller, featuring autonomous obstacle avoidance and speed control.

## 🚀 Features
* **Wireless Control:** Drive the car using a smartphone app (via Bluetooth/Wi-Fi) or a dedicated radio transmitter.
* **Obstacle Avoidance:** Equipped with ultrasonic/IR sensors to automatically detect and avoid collisions.
* **Speed Regulation:** Pulse-Width Modulation (PWM) control for smooth acceleration and turning.
* **Modular Design:** Easy to expand with additional sensors, cameras (for FPV), or robotic arms.

---

## 🛠️ Hardware Requirements
To build this bot, you will need the following components:

* **Microcontroller:** Arduino Uno / ESP32 / Raspberry Pi Pico
* **Chassis:** 2WD or 4WD Robot Car Chassis Kit
* **Motors:** 2x or 4x DC Gear Motors (with wheels)
* **Motor Driver:** L298N or L293D Motor Driver Module
* **Wireless Module:** HC-05 Bluetooth Module (or built-in ESP32 Wi-Fi)
* **Sensors:** HC-SR04 Ultrasonic Sensor (Optional for autonomous mode)
* **Power Source:** 2x 18650 Li-ion batteries (7.4V) or a 9V battery
* **Miscellaneous:** Jumper wires, switch, breadboard or custom PCB

---

## 🔌 Circuit Connection (Wiring)
*Adjust the pin configuration below based on your actual wiring setup:*

| Component | Microcontroller Pin | Motor Driver Pin |
| :--- | :--- | :--- |
| **Motor Driver (IN1)** | Pin 5 | - |
| **Motor Driver (IN2)** | Pin 6 | - |
| **Motor Driver (IN3)** | Pin 9 | - |
| **Motor Driver (IN4)** | Pin 10 | - |
| **Bluetooth RX** | Pin 3 (TX) | - |
| **Bluetooth TX** | Pin 2 (RX) | - |
| **Ultrasonic Trigger**| Pin 11 | - |
| **Ultrasonic Echo** | Pin 12 | - |

---

## 💻 Software & Setup

### Prerequisites
1. Download and install the [Arduino IDE](https://arduino.cc).
2. Install necessary libraries (e.g., `NewPing` for ultrasonic sensors if applicable).

### Installation & Flashing
1. **Clone this repository** to your local machine:
   ```bash
   git clone https://github.com
   ```
2. Open the main code file `rc_car_bot.ino` in the Arduino IDE.
3. Select your exact **Board** and **Port** from the `Tools` menu.
4. Click **Upload** to flash the code onto your microcontroller.

---

## 🎮 How to Control the Bot
1. Power on the RC car using the onboard switch.
2. Open your preferred smartphone controller app (e.g., *Arduino Bluetooth RC Car* available on Play Store/App Store).
3. Pair your phone with the **HC-05** Bluetooth module (Default pairing code is usually `1234` or `0000`).
4. Use the on-screen joysticks or directional pads to steer the bot:
   * **W / Up Arrow:** Forward
   * **S / Down Arrow:** Backward
   * **A / Left Arrow:** Turn Left
   * **D / Right Arrow:** Turn Right

---

## 📂 Project Structure
```text
rc-electric-car-bot/
├── code/
│   └── rc_car_bot.ino      # Main control firmware
├── schematics/
│   └── circuit_diagram.png # Wiring and connection layout
├── docs/
│   └── component_list.md   # Detailed hardware specifications
└── README.md               # Project documentation
```

---

## 🤝 Contributing
Contributions are welcome! If you want to optimize the speed algorithms, fix a bug, or add a line-follower feature:
1. Fork the project.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
