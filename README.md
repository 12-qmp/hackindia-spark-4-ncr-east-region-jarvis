# hackindia-spark-4-ncr-east-region-jarvis
Hackathon team repository for Jarvis - [hackindia-team:hackindia-spark-4-ncr-east-region:jarvis]

# 📡 ESP32 Smart Relay Controller (Wi-Fi + MQTT + IR + PIR)

A fully featured ESP32-based home automation system that allows you to control 4 relays using multiple interfaces:

- Web Dashboard (AP + Station mode)
- MQTT (IoT integration)
- IR Remote Control
- PIR Motion Automation

This project is designed for flexibility, offline control, and cloud integration.

---

## 🚀 Features

### Relay Control (4 Channels)
Control 4 relays independently via:
- Web interface
- MQTT topics
- IR remote

---

### Dual Wi-Fi Mode

#### Access Point (AP Mode)
- Triggered by pressing Wi-Fi button at boot
- SSID: ESP32-Control
- Password: 12345678

Includes:
- Wi-Fi setup page
- Relay control dashboard

#### Station Mode
- Connects to saved Wi-Fi
- Runs Web server + MQTT

---

### Web Interface
Routes:
/           → Relay Dashboard  
/relay      → Relay Control UI  
/wifi       → Wi-Fi Setup Page  
/toggle     → Toggle relay  
/status     → Get relay status  
/savewifi   → Save credentials  

---

### MQTT Integration

Broker: broker.hivemq.com

Topics:
home/<deviceID>/relay/1 → ON / OFF  
home/<deviceID>/relay/2 → ON / OFF  
home/<deviceID>/relay/3 → ON / OFF  
home/<deviceID>/relay/4 → ON / OFF  
home/<deviceID>/pir     → ON / OFF  

Features:
- Real-time control
- Retained state sync
- Full system synchronization

---

### IR Remote Control
- Toggle each relay
- Toggle PIR mode
- Syncs with MQTT

---

### PIR Motion Automation
- Detects motion
- Auto turn OFF relays after 10 minutes inactivity
- Can be enabled/disabled

---

### Persistent Storage
- Stores Wi-Fi credentials using Preferences (NVS)

---

### Auto Reconnect
- Wi-Fi reconnect logic
- MQTT reconnect logic

---

## 🧠 Technology Stack

### Hardware
- ESP32
- Relay Module (4 Channel)
- PIR Sensor
- IR Receiver
- Push Button
- LEDs

### Software
- Arduino Framework
- WiFi.h
- WebServer.h
- Preferences.h
- PubSubClient.h
- IRremote.hpp

### Protocols
- HTTP
- MQTT
- IR

---

## 📂 Pin Configuration

Relay 1 → GPIO 26  
Relay 2 → GPIO 27  
Relay 3 → GPIO 32  
Relay 4 → GPIO 33  
PIR Sensor → GPIO 34  
IR Receiver → GPIO 15  
Wi-Fi Button → GPIO 13  
Wi-Fi LED → GPIO 2  
PIR LED → GPIO 4  

---

## ⚙️ Setup Instructions

1. Upload code to ESP32  
2. Hold Wi-Fi button and power ON  
3. Connect to ESP32-Control Wi-Fi  
4. Open http://192.168.4.1  
5. Enter Wi-Fi credentials  
6. Device reboots  

---

## 🔍 Serial Output
Shows:
- Wi-Fi status
- MQTT topics
- Incoming messages

---

## 🔮 Future Improvements
- Mobile App
- Home Assistant Integration
- OTA Updates
- Scheduling
- Energy Monitoring

---

## 📜 License
Free to use and modify.
