---
publishDate: 2025-12-11
title: Gesture-Based Automation Hub
excerpt: A touchless 3-channel home automation system powered by APDS9960 gestures.
image: cover.jpg
tags:
  - gesture-control
  - myosa
  - automation
  - embedded-system
---

> A fully offline, touchless gesture-based controller for multi-device home automation.

---

## Acknowledgements
This project is a part of the MYOSA hardware challenge. Special thanks to the organizers for providing the development kit, guidance, and motivation to explore gesture-based control systems.

---

## Overview

This project demonstrates a **touchless gesture-controlled automation hub** that eliminates the need for physical switches or cloud-based voice assistants.  
Using the **APDS9960 gesture sensor**, a **microcontroller**, **OLED display**, and a **3-channel relay module**, the system converts simple hand movements into direct electrical control signals.

### **Problem**
Traditional automation relies on:
- Mobile apps (Wi-Fi dependency)  
- Physical switches (non-hygienic)  
- Voice assistants (privacy concerns)

### **Solution**
A fast, private, offline alternative:
- No internet  
- No physical touch  
- No voice commands  
- Works entirely on local hardware logic  

This provides a new “third modality” of interaction.

---

## Demo / Examples

### **Images**

<p align="center">
  <img src="/demo1.jpg" width="800"><br/>
  <i>Gesture detection and channel selection</i>
</p>

<p align="center">
  <img src="/demo2.jpg" width="800"><br/>
  <i>OLED feedback showing device states</i>
</p>

---

### **Videos**

<video controls width="100%">
  <source src="/demo-video.mp4" type="video/mp4">
</video>

---

## Features (Detailed)

### **1. Multi-Device Gesture Control**
The system supports **3 independent appliances** using a 3-channel relay module.  
Each appliance can be turned ON/OFF using only hand gestures.

### **2. State-Based Channel Selection (FSM Model)**
- **Swipe Left** → Previous channel  
- **Swipe Right** → Next channel  
- Selected channel stays active until changed.

This allows dedicated per-device control without confusion.

### **3. Action Gestures**
- **Swipe Up** → Turn ON active channel  
- **Swipe Down** → Turn OFF active channel  

### **4. Dynamic OLED Feedback**
The OLED display shows:
- Current active channel  
- Status of all channels:  
  - `CH1: ON/OFF`  
  - `CH2: ON/OFF`  
  - `CH3: ON/OFF`  
- Real-time pointer ( > ) that moves with left/right gestures.

### **5. Fully Offline & Low Latency**
- No Wi-Fi  
- No cloud  
- No smartphone  
- Instant response via GPIO relay control

### **6. Hygienic & Accessible**
Ideal for:
- Kitchens  
- Workshops  
- Wet/dirty environments  
- Accessibility users  

---

## Usage Instructions

1. Power the controller with the MYOSA microcontroller.
2. Swipe **Left/Right** to choose your appliance.
3. Swipe **Up** to turn it ON.
4. Swipe **Down** to turn it OFF.
5. OLED confirms each action instantly.

---

## Tech Stack

- **Microcontroller** (provided in MYOSA kit)  
- **APDS9960 Gesture Sensor**  
- **SSD1306 OLED Display (0.96”)**  
- **3-Channel Relay Module (5V)**  
- **Arduino IDE (C++ firmware)**  
- **Adafruit_APDS9960 Library**  

---

## Requirements / Installation

### **Libraries**
```bash
Adafruit_APDS9960
Adafruit_GFX
Adafruit_SSD1306
