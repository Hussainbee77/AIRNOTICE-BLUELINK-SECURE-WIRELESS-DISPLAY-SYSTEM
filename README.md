📌 Overview

AirNotice BlueLink is a secure, Bluetooth-based wireless notice board system developed using the LPC2148 microcontroller. It allows authorized users to send messages from an Android smartphone, which are verified using a passkey and displayed as scrolling text on a multi 8x8 dot-matrix LED display.

The system replaces traditional notice boards with a secure, flexible, and real-time digital solution suitable for schools, offices, and public announcement areas.

🚀 Features

📲 Android-based wireless message transmission (Bluetooth – HC-05)

🔐 Passkey-protected message authentication

💾 EEPROM-based message storage (AT25LC512)

🔄 Continuous scrolling display on 4 × 8x8 dot-matrix LEDs

⚡ UART interrupt-based communication

🛑 Auto-update display when new authorized message is received

🕒 Default message display: “Waiting for message”

🛠 Hardware Requirements

LPC2148 Microcontroller

4 × 8x8 Dot Matrix LED Displays

74HC573 (Latch)

74HC164 (Shift Register)

AT25LC512 EEPROM

HC-05 Bluetooth Module

DB-9 Cable / USB-UART Converter

💻 Software Requirements

KEIL C Compiler

Embedded C Programming

Flash Magic (for programming LPC2148)

HC-05 Terminal App (Android)

🔌 System Architecture

Android app sends message via Bluetooth.

LPC2148 receives message using UART interrupt.

System verifies passkey (e.g., $$786Vector India$$).

Valid message is stored in EEPROM.

Stored message scrolls continuously on dot-matrix display.

If no message exists → displays “Waiting for message”.
🔐 Security Format

Message must follow this syntax:

$$<PASSKEY><MESSAGE>$$

Example:

$$786Vector India$$

Displayed Output:

Vector India

Only messages with the correct passkey are accepted.
