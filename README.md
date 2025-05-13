# Smart-Watch

This repository contains the source code and documentation for the **Smart Watch** project, designed to measure and display heart rate and detect air quality levels using sensors. The project integrates with an Android application to display real-time data and features an LCD display to show relevant information.

## Project Overview

The Smart Watch project aims to create a wearable device capable of monitoring the user's heart rate, detecting dangerous gases in the environment, and displaying the time. The device will communicate with an Android application via Bluetooth to transmit data.

### Key Features

- **Heart Rate Monitoring**: Utilizes the MAX30100 heart rate sensor to measure and display the user's heart rate in real time.
- **Air Quality Monitoring**: Uses the MQ135 sensor to detect harmful gases (such as carbon dioxide) and display their concentrations.
- **Time and Date Display**: Displays the current time and date on the LCD screen.
- **Mobile Integration**: Data is sent to a mobile app via Bluetooth. The app shows the heart rate, air quality, and other relevant information.
- **Alarm System**: Displays the caller's phone number when a call is received, along with real-time heart rate information.

## Architecture

The project consists of the following components:

1. **Sensors**:
   - MAX30100 (Heart rate sensor)
   - MQ135 (Gas sensor)

2. **Microcontroller**:
   - ESP8266 for WiFi/Bluetooth connectivity

3. **LCD Display**: Displays heart rate, time, date, and air quality information.

4. **Mobile App**: Connects to the device via Bluetooth and shows the received data in real time.

5. **Web App**: Displays sensor data and stores historical information.

### Data Flow

1. The sensors (MAX30100 and MQ135) collect data from the environment.
2. Data is sent to the microcontroller (ESP8266) via Bluetooth.
3. The data is displayed on the LCD screen and sent to the mobile application.
4. The mobile app displays the heart rate, air quality data, and call information (if available).

## Getting Started

### Prerequisites

- Arduino IDE (for uploading the code to the microcontroller)
- Required Libraries:
  - `MAX30100` for heart rate sensor
  - `MQ135` for gas sensor
  - `BluetoothSerial` for Bluetooth communication
  - `LiquidCrystal` for LCD display

### Installation

1. **Clone the Repository:**

```bash
git clone https://github.com/yeganebagheri/Smart-Watch.git
cd smart-watch
