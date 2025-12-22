---
publishDate: 2025-12-11
title: Gesture-Based Automation Hub
excerpt: A touchless 3-channel home automation system powered by APDS9960 gestures.
image: demo1.jpg
tags:
  - myosa
  - gesture-control
  - automation
  - embedded-system
---

> A fully offline, touchless gesture-based controller for multi-device home automation.

---

## Acknowledgements

This project has been developed as part of the **MYOSA Hardware Challenge**.  
I would like to thank the MYOSA team for providing the hardware kit, clear guidelines, and an opportunity to explore gesture-based automation systems.

---

## Overview

The **Gesture-Based Automation Hub** is a touchless control system designed to operate multiple electrical appliances using simple hand gestures.

Unlike conventional home automation systems that rely on:
- Internet connectivity  
- Mobile applications  
- Physical switches  
- Voice assistants  

this system works **completely offline** and focuses on **privacy, hygiene, and instant response**.

Using an **APDS9960 gesture sensor**, a **microcontroller**, an **OLED display**, and a **3-channel relay module**, the system converts air gestures into direct electrical control commands without any cloud dependency.

---

## Demo / Examples

### **Images**

<p align="center">
  <img src="/demo1.jpg" width="800"><br/>
  <i>Gesture detection and channel selection using APDS9960</i>
</p>

<p align="center">
  <img src="/demo2.jpg" width="800"><br/>
  <i>OLED feedback showing active channel and device states</i>
</p>

---

### **Videos**

📽️ **Project Presentation Video**  
👉 [Click to view presentation video](presentation.mp4)

📽️ **Live Demonstration Video**  
👉 [Click to view system demonstration](demonstration.mp4)

*(Videos are uploaded locally as per MYOSA submission rules.)*

---

## Features (Detailed)

### **1. Multi-Device Gesture Control**
The system supports control of **three independent appliances** using a 3-channel relay module.  
Each appliance can be controlled individually through gesture-based commands.

---

### **2. State-Based Channel Selection (Finite State Machine)**

- **Swipe Right** → Select next channel (1 → 2 → 3 → 1)  
- **Swipe Left** → Select previous channel (1 → 3 → 2 → 1)  

Once selected, the channel remains active until another left or right gesture is detected.

---

### **3. Action Gestures**
- **Swipe Up** → Turn ON the selected channel  
- **Swipe Down** → Turn OFF the selected channel  

This separation of *selection* and *action* ensures reliable multi-device control.

---

### **4. Dynamic OLED Visual Feedback**
The OLED display continuously shows:
- Active channel indicator  
- ON/OFF status of all channels  
- Instant updates after every valid gesture  

This improves usability and prevents accidental operations.

---

### **5. Offline, Low-Latency Operation**
- No Wi-Fi  
- No cloud processing  
- No smartphone dependency  
- Instant GPIO-based relay switching  

The system responds immediately to gestures with minimal delay.

---

### **6. Hygienic and Accessible Interface**
The touchless interface makes the system suitable for:
- Hygiene-sensitive environments  
- Workshops and labs  
- Wet or dusty conditions  
- Users with limited motor control  

---

## Usage Instructions

1. Power the system using the MYOSA microcontroller.
2. Perform **left or right swipe** to select the desired appliance.
3. Perform **up swipe** to turn the appliance ON.
4. Perform **down swipe** to turn the appliance OFF.
5. Observe real-time feedback on the OLED display.

---

## Tech Stack

- **Microcontroller** (MYOSA Kit)  
- **APDS9960 Gesture Sensor**  
- **SSD1306 OLED Display (0.96 inch)**  
- **3-Channel Relay Module (5V)**  
- **Arduino IDE (C++ firmware)**  
- **Adafruit_APDS9960 Library**  

---

## Requirements / Installation

### **Libraries Required**
```bash
Adafruit_APDS9960
Adafruit_GFX
Adafruit_SSD1306
