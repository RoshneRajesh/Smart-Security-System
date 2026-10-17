# Smart Security System 🔐

An Arduino and ESP8266-based IoT Smart Security System designed to safeguard a home environment. This project provides dual authentication (RFID and PIN) for access control and utilizes a PIR sensor to send real-time motion alerts via a Telegram Bot.

## 👥 Team Members
*   Krishna Priya Gopalan (BL.SC.U4CSE24224)
*   Roshne Rajesh (BL.SC.U4CSE24241)

**Course:** 23CSE201 - Procedural Programming using C  
**Institution:** Amrita School of Engineering, Bangalore

## ✨ Features
*   **Dual Authentication:** Access granted via RFID card scan or 4x4 Keypad PIN entry.
*   **Intrusion Detection:** PIR motion sensor detects movement.
*   **Real-time Alerts:** ESP8266 NodeMCU sends instant Telegram notifications when motion is detected.
*   **Feedback Mechanisms:** Audio (buzzer) and visual (Red/Green LEDs) indicators for access granted/denied.
*   **Physical Locking:** Servo motor acts as a smart door lock.

## 🛠️ Hardware Components
*   Arduino Uno (Main Controller)
*   ESP8266 (NodeMCU) (Wi-Fi & Telegram Bot)
*   MFRC522 RFID Module
*   4x4 Hex Keypad
*   PIR Motion Sensor
*   Servo Motor (Door Lock)
*   Active Low Buzzer
*   LEDs (Red and Green)
*   220Ω Resistors

## 🔌 Pin Connections

### Arduino Uno
| Component | Pin | Arduino Pin |
| :--- | :--- | :--- |
| **RFID** | VCC, GND, RST, SDA, SCK, MOSI, MISO | 3.3V, GND, D9, D10, D13, D11, D12 |
| **Keypad** | Rows 1-4 | D2, D3, D4, D5 |
| **Keypad** | Cols 1-4 | D6, D7, A1, A0 |
| **Servo** | Signal, VCC, GND | A4, 5V, GND |
| **Buzzer** | Signal | D8 |
| **Green LED** | Anode, Cathode | A2, GND |
| **Red LED** | Anode, Cathode | A3, GND |

### ESP8266 (NodeMCU)
| Component | Pin | NodeMCU Pin |
| :--- | :--- | :--- |
| **PIR Sensor** | VCC, GND, OUT | 3.3V/5V, GND, D5 (GPIO 14) |

## 🚀 How to Run

1. **Arduino Uno:**
   * Open `src/Arduino_Uno/Arduino_Uno.ino` in the Arduino IDE.
   * Install the `MFRC522`, `Keypad`, and `Servo` libraries via the Library Manager.
   * Upload to the Arduino Uno.
2. **ESP8266:**
   * Open `src/ESP8266_NodeMCU/ESP8266_NodeMCU.ino` in the Arduino IDE.
   * Install the `UniversalTelegramBot` and `ArduinoJson` libraries.
   * Update the `ssid`, `password`, `BOTtoken`, and `CHAT_ID` with your own credentials.
   * Upload to the NodeMCU.

## 📸 Outputs
*   **Serial Monitor:** Shows authentication status and PIN entry.
*   **Telegram Bot:** Sends "Bot started up" and "Motion detected!!" messages.

## 📄 Documentation
The complete project report is available in the `docs/` folder.
