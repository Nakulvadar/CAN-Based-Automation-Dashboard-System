# CAN Based Automation Dashboard System

## 📌 Overview

This project implements a **multi-node embedded dashboard system** using the **Controller Area Network (CAN) protocol**. It simulates real-time automotive ECU communication by transmitting and displaying parameters like **speed, gear position, RPM, and indicator status**.

---

## ⚙️ Features

* Real-time **Speed Monitoring (ADC-based)**
* **Gear Position Detection (Switch input)**
* **RPM Calculation (ADC scaling)**
* **Indicator Control (Left/Right/Off)**
* **CAN Communication (Tx/Rx using Message IDs)**
* **CLCD & 7-Segment Display Interface**
* Modular driver-based architecture

---

## 🧠 System Architecture

The system consists of multiple ECU nodes:

### 🔹 Transmitter Node (ECU1)

* Reads speed using ADC
* Detects gear position
* Transmits speed & gear via CAN

### 🔹 Sensor Node (ECU2)

* Calculates RPM from ADC
* Controls indicator system
* Transmits RPM & indicator status via CAN

### 🔹 Receiver Node (Dashboard ECU)

* Receives CAN messages
* Decodes message IDs
* Displays data on CLCD
* Controls indicator LEDs

---

## 🔁 Data Flow

Sensor Input → Microcontroller → CAN Tx → CAN Bus → CAN Rx → Dashboard Display

---

## 🔌 Hardware Components

* PIC Microcontroller
* MCP2515 CAN Module
* CLCD Display
* 7-Segment Display (SSD)
* Potentiometer (Speed/RPM simulation)
* Switches (Gear & Indicators)

---

## 🛠️ Technologies Used

* Embedded C
* MPLAB X IDE
* CAN Protocol (CAN 2.0)
* UART (Debugging)

---

## 📂 Project Structure

* `src/` → Application logic
* `drivers/` → CAN, ADC, CLCD, UART
* `inc/` → Header files
* `docs/` → Diagrams & design
* `images/` → Output screenshots

---

## 🚀 How to Run

1. Open project in **MPLAB X IDE**
2. Build and flash code to PIC microcontrollers
3. Connect CAN nodes via MCP2515
4. Power ON system
5. Observe real-time dashboard output

---

## 📸 Output

(Add screenshots of CLCD display, SSD output, and hardware setup in `/images` folder)

---

## 📈 Future Improvements

* ESP8266 integration for web dashboard
* Cloud data logging
* Fault detection system
* Mobile app interface

---

## 👨‍💻 Author

**Nakul Anil Vadar**

---
