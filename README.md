# 🌾IoT-Agricultural-Automation
An IoT-based smart farming system designed to automate irrigation and monitor environmental conditions using Arduino Nano, ESP8266, NRF24L01, and cloud APIs. This project enables real-time monitoring, long-range wireless data transfer, and intelligent irrigation control using schedules, thresholds, and manual overrides.

## ⭐ Features

 Wireless long-range communication using NRF24L01

  Sensor monitoring:

        1.Soil Moisture
  
        2.Temperature

        3.Humidity

        4.Light Intensity

 Real-time dashboard via Mobile App (MIT App Inventor) and Web UI

  Automated irrigation based on:

        1.Moisture threshold

        2.Scheduled time

        3.Manual user control

 Cloud integration using PHP + MySQL (ATSPACE hosting)

 Low power consumption suitable for agricultural fields

## 🛠 Hardware Components

Arduino Nano (Slave Node)

ESP8266 NodeMCU (Master Node)

NRF24L01 Wireless Modules

Soil Moisture Sensor

LDR Sensor

DHT11 Temperature & Humidity Sensor

Relay Module + Water Pump

Li-ion Battery 

## 🔧 Software / Tools Used

Arduino IDE

ATSPACE Hosting (PHP + MySQL)

MIT App Inventor (Android App)

HTTP API (GET requests)

JSON Data Parsing

HTML/PHP for cloud interface

## 📡 System Architecture
1. Slave Node (Arduino Nano)

Reads sensor data

Sends data wirelessly via NRF24L01

2. Master Node (ESP8266)

Receives the data

Uploads to cloud APIs

Fetches irrigation schedule and threshold

Controls relay + pump

3. Cloud Server

Stores sensor data

Stores irrigation commands

Provides APIs for app & ESP8266

4. Mobile App

Displays real-time data

Allows scheduling

Manual pump control

Threshold update

## 🚀 Key API Endpoints
GET /api/led/read_all.php?id=10     → Read pump control settings  
GET /api/led/update.php?id=8        → Upload soil moisture & temperature  
GET /api/led/update.php?id=9        → Upload brightness & humidity  
GET /api/led/update.php?id=10       → Update schedule/thresh/pump state  

## 🔌 Irrigation Logic

Manual Mode: ON/OFF pump directly from app

Scheduled Mode: Pump turns ON/OFF at user-defined time

Automatic Mode: Pump activates when

Soil Moisture < Threshold


ESP8266 uploads changes back to server

## 📱 Mobile App Features

Real-time sensor dashboard

Pump ON/OFF control

Schedule setup (hour, minute, state)

Moisture threshold configuration

Refresh button for live data

## 📷 Screenshots

Include:

App UI

Block diagram

Circuit diagrams

ATSPACE API dashboard

### 📚 Conclusion

This project provides a practical, low-cost, and scalable solution for smart farming. By combining low-power wireless sensor nodes, cloud automation, and a mobile app interface, the system enhances irrigation efficiency, conserves water, and reduces manual farming workload.
