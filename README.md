## 🚦 Automatic Traffic Light Control System with IR Sensors – README

### 📘 Overview
This project demonstrates a **smart traffic light system** using **IR sensors** and an **Arduino Uno** to dynamically control signal timing based on vehicle presence. Unlike traditional timed signals, this system reduces unnecessary waiting and improves traffic flow by detecting real-time vehicle density.

### 🔍 System Description
The system uses **Infrared (IR) sensors** to detect vehicles at intersections. When a vehicle is detected, the Arduino processes the input and adjusts the traffic light sequence accordingly.

| Component        | Description                                                  |
|------------------|--------------------------------------------------------------|
| IR Sensor        | Detects vehicle presence using reflected infrared light      |
| Arduino Uno      | Central controller that processes sensor input and controls lights |
| Traffic Lights   | LEDs (Red, Yellow, Green) representing signal states         |
| I2C LCD (optional) | Displays traffic status or countdown timers                |

### 🧠 Internal Structure

#### 🔧 IR Sensor
- **Emitter (IR LED)**: Sends out infrared light.
- **Receiver (Photodiode)**: Detects reflected IR light from nearby vehicles.
- **Comparator Circuit**: Converts analog signal to digital output.
- **Adjustable Potentiometer**: Sets detection range.

#### 🧠 Arduino Logic
- Reads digital signals from IR sensors.
- Prioritizes lanes with detected vehicles.
- Controls traffic light LEDs via digital output pins.
- Optional: Displays status on I2C LCD screen.

### 🔌 Circuit Connections with Arduino Uno

#### 🛠️ Components Required
- Arduino Uno
- 2–4 IR sensors
- Red, Yellow, Green LEDs (per lane)
- Resistors (220Ω for LEDs)
- Jumper wires
- Breadboard
- Optional: I2C LCD 16x2 display

#### ⚡ Wiring Diagram

| IR Sensor Pin | Function       | Arduino Uno |
|---------------|----------------|-------------|
| VCC           | Power          | 5V          |
| GND           | Ground         | GND         |
| OUT           | Digital Output | D2, D3, etc.|

| LED Color | Lane 1 Pin | Lane 2 Pin |
|-----------|------------|------------|
| Red       | D8         | D11        |
| Yellow    | D9         | D12        |
| Green     | D10        | D13        |

> 💡 Tip: Use separate digital pins for each LED to control them independently.

### 📦 Applications
- Smart city traffic management
- Emergency vehicle prioritization
- Parking lot automation
- School zone safety systems
