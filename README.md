# ESP32 Timer Interrupt Example

This project demonstrates how to use a **hardware timer interrupt on the ESP32** using **PlatformIO and the Arduino framework**.

The ESP32 generates periodic interrupts internally, without any external input, and counts how many times the interrupt occurs.

---

## 🚀 Features

* Hardware timer interrupt (ESP32)
* Periodic execution (1 second interval)
* Interrupt Service Routine (ISR)
* Thread-safe variable handling using critical sections
* Serial output for real-time monitoring

---

## 🛠️ Hardware Requirements

* ESP32 development board
* USB cable

No external components are required.

---

## ⚙️ Development Environment

* **IDE:** Visual Studio Code
* **Extension:** PlatformIO
* **Framework:** Arduino
* **Board:** ESP32 Dev Module

---

## 📁 Project Structure

```
project/
├── platformio.ini
├── src/
│   └── main.cpp
└── README.md
```

---

## ⚡ How It Works

1. A hardware timer is initialized using `timerBegin()`.
2. An interrupt is attached using `timerAttachInterrupt()`.
3. The timer is configured to trigger every **1 second**.
4. Each interrupt executes an **ISR**, incrementing a counter.
5. The main loop processes the interrupt and prints the total count.

---

## 🧠 Key Concepts

* Hardware timers
* Interrupt Service Routine (ISR)
* `volatile` variables
* Critical sections (`portENTER_CRITICAL`)
* Periodic interrupts

---

## 🖥️ Example Output

```
An interrupt has occurred. Total number: 1
An interrupt has occurred. Total number: 2
An interrupt has occurred. Total number: 3
```

The counter increases automatically every second.

---

## 📌 Notes

* The interrupt is generated internally by the ESP32 timer
* No external input (buttons or sensors) is required
* The interval can be modified by changing the timer configuration

---

## 📚 Technologies Used

* ESP32
* C++
* PlatformIO
* Arduino Framework

---

## 🎯 Purpose

Educational example to understand how **timer-based interrupts** work on ESP32 and how they differ from GPIO-based interrupts.

---
