# Arduino-servo-motor
This project uses an **Arduino UNO** board to control **four servo motors** using **four push buttons** connected on a breadboard.
# 🤖 Arduino-Based Multi-Servo Control System

A compact and scalable servo motor control system built with **Arduino UNO**, designed to demonstrate real-time input/output interaction using hardware buttons. This project highlights key skills in embedded systems, circuit design, and C++ microcontroller programming — making it an excellent portfolio piece for roles in robotics, mechatronics, or automation.

---

## 🧩 Project Overview

This system controls **four servo motors** independently using **four push buttons**. Pressing any button will trigger its corresponding motor to rotate to a defined angle (e.g. 90°). Once released, the servo returns to its neutral position.

> ⚡ This mimics real-world use cases like robotic joints, automated levers, or interactive mechanical systems.

---

## 📦 Hardware Components

| Qty | Component                     | Notes                                      |
|-----|-------------------------------|--------------------------------------------|
| 1   | Arduino UNO                   | Microcontroller board                      |
| 4   | SG90 Servo Motors             | PWM-based rotational actuators             |
| 4   | Push Buttons                  | Used as input switches                     |
| 4   | 10kΩ Resistors                | For stable digital input via pull-up       |
| 1   | Breadboard + Jumper Wires     | Circuit prototyping and connections        |
| 1   | 5V External Power Supply (2A) | Recommended for simultaneous servo use     |
| 1   | 100μF Capacitor (Optional)    | Helps smooth power delivery to servos      |

---

## 🛠️ Tools & Libraries

- Arduino IDE (v2.x recommended)
- Built-in `Servo.h` library
- Tinkercad (or Fritzing) for circuit simulation and diagramming

---

## ⚙️ System Behavior & Logic

The system follows a **modular input/output model**:

- Each push button is connected to a digital input using `INPUT_PULLUP` mode.
- Each servo is connected to a PWM-compatible digital output (Pins 6–9).
- When a button is pressed, the microcontroller writes a **90° angle** to the respective servo.
- Releasing the button sends the servo back to **0°** (default rest position).

This ensures responsive, real-time actuation and can be expanded to include sensors or communication modules.

### 🧠 Control Logic Flow

```cpp
if (digitalRead(buttonPin) == LOW) {
  servo.write(90);  // Rotate servo
} else {
  servo.write(0);   // Reset position
}
```

---

## 🚀 Getting Started

### 🖇️ Hardware Setup
1. Connect each servo's signal pin to pins 6, 7, 8, and 9.
2. Connect buttons to pins 2, 3, 4, and 5.
3. Connect servo power lines to 5V (preferably via an external supply).
4. Add pull-down resistors or use `INPUT_PULLUP` in code.

### 💻 Software Upload
1. Open Arduino IDE.
2. Paste the code or use the provided file.
3. Select the correct board and port.
4. Upload the code and test each button.

---

## 💾 Source Code

🔗 [View the full Arduino code here](https://github.com/Safwan-Aleman/Arduino-servo-motor/blob/main/Servo-code/Servo-code.ino)

---

## 🎯 Project Highlights

- ✅ Real-time digital input processing  
- ✅ PWM-based servo motor control  
- ✅ Clean modular hardware layout  
- ✅ Built-in debounce using `INPUT_PULLUP`  
- ✅ Expandable to 6+ servos or sensor-based input  

---

## 🖼️ Circuit Diagram

<img src="showcase/demo-circuit.png" alt="Circuit Diagram" style="max-width: 100%;">

---

## 🎥 Demo Video

<img src="showcase/demo-circuit.png" alt="Circuit Diagram" style="max-width: 100%;">

---

## 📁 Folder Structure

```
project-root/
├── showcase/
│   ├── demo-circuit.png
│   └── demo.mp4
├── Servo-code/
│   └── Servo-code.ino
└── README.md
```

---

## 🧠 Skills You Demonstrate

- Embedded C++ (Arduino)
- Hardware-software integration
- PWM signal control
- Real-time event handling
- Circuit design and simulation
- Portfolio documentation & clarity

---


## 👤 Author

**Your Name Here**  
GitHub: [@Safwan-Aleman](https://github.com/Safwan-Aleman)  

---

> ✅ *Ready for interviews. Ready for GitHub. Ready to impress.*
