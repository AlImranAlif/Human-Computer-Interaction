# 📡 RFID-Based Electronic Voting Machine (HCI Project)

A Human-Computer Interaction (HCI) based electronic voting system built using **Arduino Uno**, **RC522 RFID module**, and **SSD1306 OLED display**.  
The system demonstrates how **usability, feedback, and error prevention** can be implemented in a low-cost embedded system.

---

## 👨‍🎓 Team Members

- Arafat Hossain (23-50277-1)  
- Rajarshi Mondal (23-50279-1)  
- Al Imran Alif (23-50273-1)  
- Tousif Tarik (23-53577-3)  

🏫 American International University-Bangladesh (AIUB)  
👨‍🏫 Supervisor: Dr. Muhammad Firoz Mridha  

---

## 📌 Project Overview

This project is a **low-cost RFID-based voting machine** designed for HCI evaluation.  
It allows users to vote securely using RFID cards and provides **real-time feedback via OLED display, LED, and buzzer**.

### 🔑 Key Features

- RFID-based voter identification  
- One-button candidate selection  
- Hold-to-confirm voting mechanism  
- OLED real-time interface  
- Live vote counting  
- Double-vote prevention system  
- Multimodal feedback (visual + audio)  
- State machine-based system design  

---

## 🖼️ System Preview
![dashboard]_("C:\Users\Alif\Downloads\WhatsApp Image 2026-05-21 at 4.49.31 AM.jpeg")


### 🔹 OLED Interface
![OLED Interface](images/oled_interface.jpg)

### 🔹 Candidate Selection Screen
![Selection Screen](images/selection_screen.jpg)

### 🔹 Hardware Wiring
![Wiring Diagram](images/wiring_diagram.jpg)

---

##  Hardware Components

- Arduino Uno R3  
- RC522 RFID Module (13.56 MHz)  
- SSD1306 OLED Display (128×64 I2C)  
- Push Button  
- LED Indicator  
- Active Buzzer  
- Breadboard & Jumper Wires  

---

##  HCI Principles Implemented

✔ Visibility of system status  
✔ Error prevention (hold-to-confirm voting)  
✔ User control & freedom (timeout system)  
✔ Recognition over recall (displayed options)  
✔ Minimal cognitive load UI design  
✔ Multimodal feedback (OLED + buzzer + LED)  

---

##  System Architecture

The system is designed using a **Finite State Machine (FSM)**:

- Non-blocking logic using `millis()`
- Button works in multiple modes (short press & long press)
- UID-based voter tracking stored in SRAM

---

##  How It Works

1. User scans RFID card  
2. System checks if voter already voted  
3. Candidate selection screen appears  
4. Button is used to cycle candidates  
5. Long press confirms vote  
6. Vote is stored and feedback is shown  
7. System returns to IDLE mode  

---

##  Anti-Vote Fraud System

- Each RFID card has a unique UID  
- Duplicate voting is blocked immediately  
- UID stored after successful vote  
- Confirmation requires long press (2 seconds)  

---

##  Performance

- RFID scan time: < 100 ms  
- Button response: ~1 ms  
- Voting duration: ~5–8 seconds  
- Real-time OLED updates  

---

##  Libraries Used

- MFRC522 RFID Library  
- Adafruit SSD1306 Library  
- Adafruit GFX Library  
- SPI & Wire (Arduino Core)

---




