# SPI Slave Communication – PIC16F877A

This project demonstrates how to implement **SPI Slave mode** communication using the **PIC16F877A**. The slave receives data from an SPI master and displays it on **PORTB**.

## 👨‍💻 Author
**Edvin Jose Vakaparamban**  
📅 Created on: [Your Date]

---

## 🔧 Overview

- SPI is configured in **Slave mode** with SS enabled.
- Received 8-bit data from the master is read via interrupt.
- The data is immediately shown on **PORTB** (LEDs or logic analyzer).
- Ideal for validating SPI functionality in multi-MCU projects.

---

## 🧰 Hardware Requirements

- PIC16F877A Microcontroller
- Master SPI device (e.g., another PIC or Arduino)
- LEDs or logic analyzer on PORTB
- SPI wiring (SCK, MISO, MOSI, SS)
- 16 MHz crystal oscillator

---

## ⚙️ Configuration

| Setting           | Value     |
|------------------|-----------|
| SPI Mode         | Slave     |
| Clock Polarity   | CKP = 1   |
| Clock Phase      | CKE = 1   |
| Sampling         | SMP = 1   |
| SDO (Out)        | RC5       |
| SDI (In)         | RC4       |
| SCK (In)         | RC3       |
| SS (In)          | RA5       |

---

## 🔄 Workflow

1. Master sends an 8-bit data byte over SPI.
2. Slave receives it via **SSPBUF** (interrupt-based).
3. Data is shown live on **PORTB**.
4. PORTB can be connected to LEDs for visual output.

---

## 🚦 Functional Flow

- Master sends ➡ Slave receives ➡ Data shown on PORTB

---


