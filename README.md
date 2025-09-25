# Smart-Water-Level-Indicator-with-Temperature-Monitoring-using-ESP32-ESP-NOW-
This project presents a low-cost, wireless IoT solution for monitoring water levels and temperature in overhead tanks using ESP32 microcontrollers. It uses ESP-NOW protocol for wireless data transfer, an ultrasonic sensor for water level detection, a DS18B20 sensor for temperature measurement, and a 16x2 LCD + buzzer for display and alerts.

## 📌 Overview

This project presents a **low-cost, wireless IoT solution** for **water level and temperature monitoring** in household water tanks.
It uses **ESP32 microcontrollers** with the **ESP-NOW protocol** for fast, peer-to-peer communication, an **ultrasonic sensor** for water level detection, and a **DS18B20 temperature sensor** for temperature monitoring.

The system provides **real-time updates** on a **16x2 LCD** and triggers a **buzzer alarm** at critical thresholds (overflow or low water levels), making it especially useful for **elderly users and households**.

---

## ✨ Features

✔️ Wireless communication (ESP-NOW – no Wi-Fi required)
✔️ Real-time water level detection with ultrasonic sensor
✔️ Temperature monitoring using DS18B20 sensor
✔️ LCD display for user-friendly interface
✔️ Buzzer alerts at >90% (overflow risk) and <10% (low water risk)
✔️ Energy-efficient and low-cost design

---

## 🛠️ Hardware Requirements

* 2 × ESP32 Development Boards
* 1 × Waterproof Ultrasonic Sensor (HC-SR04 / JSN-SR04T)
* 1 × DS18B20 Digital Temperature Sensor
* 1 × 16x2 LCD with I2C Module
* 1 × Buzzer
* Jumper wires, Breadboard, Power supply

---

## 💻 Software Requirements

* **Arduino IDE**
* **ESP32 board package** installed in Arduino IDE
* Required libraries:

  * `esp_now.h`
  * `WiFi.h`
  * `LiquidCrystal_I2C.h`
  * `OneWire.h`
  * `DallasTemperature.h`

---

## ⚙️ System Architecture

1. **Transmitter ESP32**

   * Reads water level using ultrasonic sensor
   * Sends data wirelessly via ESP-NOW

2. **Receiver ESP32**

   * Displays water level on LCD
   * Reads water temperature from DS18B20 sensor
   * Activates buzzer for critical thresholds

3. **User Interface**

   * LCD shows real-time water level (%) and temperature (°C / °F)
   * Buzzer provides alerts for overflow or dry condition

---

## 🚀 Setup & Usage

1. Install **Arduino IDE** and add **ESP32 board support**.
2. Upload `transmitter.ino` to the first ESP32 (connected to ultrasonic sensor).
3. Upload `receiver.ino` to the second ESP32 (connected to LCD + buzzer + DS18B20).
4. Power both ESP32 boards and place the ultrasonic sensor in the overhead tank.
5. LCD will display **Water Level (%) + Temperature (°C/°F)**.
6. Buzzer will alert if water level is **too high (>90%)** or **too low (<10%)**.

---

## 📊 Results

* Water level accurately displayed in real time (Empty → Low → Medium → High → Full).
* Temperature readings accurate within ±1°C.
* ESP-NOW communication stable up to **10–15 meters**.
* Low-cost, scalable, and easy-to-install system.

---

## 🔮 Future Enhancements

* Add **water quality sensors** (TDS, pH)
* **Mobile app / cloud integration** for remote monitoring
* **Automatic motor control** for pumping water
* Extend communication range using **LoRa / Zigbee**
* Integration with **smart home systems (Google Home, Alexa)**

---


