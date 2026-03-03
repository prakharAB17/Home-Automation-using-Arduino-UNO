# Bluetooth-Based Home Automation using Arduino UNO

## Overview
Designed and implemented a Bluetooth-controlled home automation system using Arduino UNO and HC-05. The system enables wireless ON/OFF control of AC appliances via an Android application.

## System Architecture
Smartphone App → HC-05 (UART @ 9600 bps) → Arduino UNO (ATmega328P) → 4-Channel Relay → AC Loads

## Key Features
- Wireless appliance control (up to 4 loads)
- UART serial communication
- Relay-based AC switching with isolation
- Low-cost embedded solution

## Hardware Used
- Arduino UNO
- HC-05 Bluetooth Module
- 4-Channel Relay Module
- AC Bulb/Fan
- 5V Power Supply

## Working
- Android app sends character commands via Bluetooth.
- Arduino reads serial input.
- Corresponding GPIO pins toggle relay states.
- Relay switches AC appliances ON/OFF.

## Communication Details
- Protocol: UART
- Baud Rate: 9600
- Command-based control (e.g., 'A' → Relay ON, 'a' → Relay OFF)

## Project Setup

![Hardware Setup 1](images/setup1.jpg)
![Hardware Setup 2](images/setup2.jpg)

## Code
Available in:
`Arduino_Code/home_automation.ino`

## Engineering Considerations
- Proper grounding between modules
- Isolation of low-voltage and AC circuits
- Stable regulated power supply

## Future Improvements
- Wi-Fi (ESP8266/ESP32) integration
- Energy monitoring using current sensor
- Cloud logging / IoT dashboard
