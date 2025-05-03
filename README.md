# Accident-Prevention

# Alcohol Detection and Vehicle Immobilization with Real-time Alert and Word Database Logging 🚗🛑

## Project Overview
This IoT-based system aims to prevent drunk driving by detecting alcohol levels near the driver, automatically immobilizing the vehicle, sending real-time alerts via email, and logging the incident to a cloud database (ThingSpeak). 

## 🔧 Hardware Components
| Component       | Description                          |
|----------------|--------------------------------------|
| ESP32 Dev Board| Wi-Fi-enabled microcontroller         |
| MQ-3 Sensor    | Alcohol gas sensor (analog + digital) |
| L293D Driver   | Motor control                         |
| DC Motor       | Vehicle movement simulation           |
| Push Button    | Manual motor ON/OFF switch            |
| 12V Power Supply | Powers motor & ESP32                |

## 📡 Working Principle
1. User starts the vehicle using a push button.
2. MQ-3 sensor continuously monitors alcohol levels.
3. If alcohol is detected:
   - Motor speed reduces gradually to simulate safe braking.
   - An alert email is sent to traffic authorities.
   - Incident is logged to **ThingSpeak** with:
     - Timestamp  
     - Vehicle registration  
     - Owner name  
     - License number  
     - System ID and IMEI  
4. If no alcohol is detected, motor runs normally.

## 💻 Technologies Used
- **ESP32**
- **MQ-3 Alcohol Sensor**
- **SMTP Email via ESP Mail Client**
- **ThingSpeak Cloud API**
- **C++**

## 📤 Cloud Logging (ThingSpeak)
- API Key and fields configured to log:
  - `field1`: Vehicle Reg. No.
  - `field2`: Owner Name
  - `field3`: License No.
  - `field4`: Vehicle Type
  - `field5`: System ID
  - `field6`: IMEI

## 📧 Email Alert
- Sent via Gmail SMTP
- Contains:
  - Vehicle & owner details
  - Time of detection
  - System and IMEI info
  - HTML formatted email for clarity

👉 [Prototype and Output](https://drive.google.com/file/d/1UC8FUfdTYsdqpWJV1scYbbeI6nCRlFEG/view?usp=sharing)

## 🚀 How to Run
1. Open project in **Arduino IDE**
2. Install required libraries:
   - `ESP Mail Client`
   - `WiFi`
   - `HTTPClient`
3. Update:
   - Wi-Fi SSID and Password
   - Gmail App Password (2FA enabled)
   - ThingSpeak API Key
4. Upload to ESP32
5. Monitor Serial Output @ 115200 baud

## 📝 Note
This project is for academic/research purposes and simulates vehicle immobilization with a DC motor. In real-world applications, additional safety and legal considerations must be addressed.

---

> **"Ensuring Safe Roads with Smart Technology!"**
