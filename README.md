# fall-detection-system

This project is a sample yet effective fall detection system using an MPU6050 accelerometer, an arduino uno and an active buzzer. The system continuously monitors acceleration and detects sudden movements that may indicate a fall . If a fall is detected, a buzzer is triggered to alert nearby individuals. 

## Features

- Real-time fall detection
- Audible alert via buzzer
- Simple hardware setup
- Optional Python script for data analysis

## Hardware Required
- Arduino Uno R3
- MPU6050 Accelerometer Module
- Active Buzzer
- Jumper wires (Male to female)

## Circuit diagram 

![Circuit Diagram](images/circuit_diagram.png)

## Setup Instructions

1. Connect the components as per the circuit diagram.
2. Upload the Arduino sketch located in `ArduinoCode/fall_detection.ino` to your Arduino board.
3. Open the Serial Monitor (9600 baud) to observe real-time acceleration values and fall detection status.
4. (Optional) Use the Python script in `PythonAnalysis/analyze_falls.py` to analyze collected data.

## Fall Detection Logic

The system calculates the total acceleration vector magnitude using the formula:


A fall is detected when this value either drops significantly (free fall) or spikes (impact), based on a threshold.

## Python Data Analysis (Optional)

You can log acceleration data from the Serial Monitor into a CSV file and use the Python script to plot the data.

```bash
pip install pandas matplotlib
python PythonAnalysis/analyze_falls.py
