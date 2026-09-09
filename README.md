# Security-System---Arduino-Uno
# Smart Security System with Arduino


⚡ Key Features:
Real-time proximity monitoring
Automated Security Trigger
  -Intermittent buzzer alarm and dynamic state LED indicators (Red/Yellow).
  * Physical barrier deployment using a Servo motor (rotates to 180°).
  * Instant status update on the LCD 1602 display:" System: blocked ".
IR Authentication & Unlocking:
  * Captures and decodes incoming infrared signals from an IR remote.
  * Verifies custom hexadecimal passcodes to switch system state to "UNLOCKED".
  * Displays "Wrong Pass" feedback upon receiving invalid infrared payloads.

🔌 Hardware Configuration & Pinout

| Hardware Component | Mode / Protocol | Arduino Pin | Description |
| :--- | :--- | :--- | :--- |
| **LCD 1602 (I2C)** | SDA / SCL | A4 / A5 | Address `0x27` |
| **HC-SR04 (Trig)** | Digital Output | Pin 9 | Ultrasonic trigger signal |
| **HC-SR04 (Echo)** | Digital Input | Pin 10 | Ultrasonic echo pulse |
| **IR Receiver** | Digital Input | Pin 11 | Remote control signal input |
| **Servo Motor** | PWM Output | Pin 6 | Physical lock mechanism (0° - 180°) |
| **Buzzer** | Digital Output | Pin 8 | Audio feedback & alarm |
| **LED 1 (Green)** | Digital Output | Pin 3 | Unlocked state indicator |
| **LED 2 (Yellow)** | Digital Output | Pin 4 | Alarm / Blocked state indicator |
| **LED 3 (Red)** | Digital Output | Pin 5 | Standby / System OK indicator |

📚 External Libraries
[`Servo.h`](https://www.arduino.cc/reference/en/libraries/servo/)
[`IRremote`](https://github.com/Arduino-IRremote/Arduino-IRremote)
[`Wire.h`](https://www.arduino.cc/en/Reference/Wire)
[`LiquidCrystal_I2C`](https://github.com/johnrickman/LiquidCrystal_I2C)

