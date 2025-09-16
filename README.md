# Neuro Nudge

A rhythm-based therapeutic game that promotes physical activity and monitors heart rate in bedridden delirium patients.

![Neuro Nudge Banner](https://private-user-images.githubusercontent.com/168996502/415816197-3ddde5bc-70d1-4625-9e34-8e3727bbfdab.jpg?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTgwNjQ3NzAsIm5iZiI6MTc1ODA2NDQ3MCwicGF0aCI6Ii8xNjg5OTY1MDIvNDE1ODE2MTk3LTNkZGRlNWJjLTcwZDEtNDYyNS05ZTM0LThlMzcyN2JiZmRhYi5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwOTE2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDkxNlQyMzE0MzBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hMmFkMzJkNzE2NGVjMzI5ZWZlNjg4MTljMjZmZGNhMWM0NzlmNTUzZmNkNzA5YTAyMzhlMDQ5MTNiMGY4MmNhJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.EdMRz4YVvipI4XjjwSuB8SMzY1K7W7VSFycRaVr5Z8c) <!-- Replace with actual image path -->

## Award-Winning Innovation

Neuro Nudge was developed in just 36 hours during a healthcare-focused hackathon. The project won the Safest Hack Award among 65+ participants for its novel use of pulse oximetry to safely engage patients in physical activity.

## Problem Statement

Delirium and immobility are significant challenges in hospital settings, especially for bedridden patients. Lack of movement can lead to rapid functional decline, prolonged recovery, and increased risk of complications.

Neuro Nudge addresses this issue by:
- Encouraging gentle, gamified physical activity
- Monitoring patient heart rate in real-time
- Providing feedback and motivation through a rhythm-based game

## Key Features

- Interactive rhythm game  
  Custom-designed interface encourages patients to move to musical cues, increasing physical activity through engaging gameplay.

- Real-time movement tracking  
  Integrates an Arduino, accelerometer, and pulse oximeter to detect limb movement and track user engagement.

- Heart rate monitoring  
  Uses pulse oximetry to detect irregularities and dynamically adjust game difficulty or provide warnings to ensure patient safety.

- Dynamic feedback loop  
  Game difficulty and prompts are responsive to movement frequency and heart rate changes, helping maintain safe exertion levels.

## Tech Stack

| Component        | Technology |
|------------------|------------|
| Frontend         | React.js, HTML, CSS |
| Backend          | Python |
| Hardware         | Arduino Nano, Pulse Oximeter, Accelerometer (MPU6050) |
| Communication    | Serial (USB) |
| Data Processing  | Custom Python script for signal filtering and feature extraction |
| Game Engine      | Web-based rhythm game synced with real-time sensor data |

## Screenshots

### Game Interface and Hardware Setup
![Game Interface](https://private-user-images.githubusercontent.com/168996502/415816185-c55f23c1-662b-4c44-bab6-1afc1b327744.jpg?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTgwNjQ3NzAsIm5iZiI6MTc1ODA2NDQ3MCwicGF0aCI6Ii8xNjg5OTY1MDIvNDE1ODE2MTg1LWM1NWYyM2MxLTY2MmItNGM0NC1iYWI2LTFhZmMxYjMyNzc0NC5qcGc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwOTE2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDkxNlQyMzE0MzBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iZWRkNmJmY2MxMzM1OGFiZWEzYmIxMGQ2YjA2NmJhYzAzZjNlMTFlM2E4ODNlZWZmZTMxZjc2NGU1OTEwYWYzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.b7adCz3ibghjUkisNqM9rmct9pLgZiw2O25xoRrhKDY) <!-- Replace with actual image path -->

## Clinical Motivation

The project was designed with input from clinical insights on delirium management, focusing on:
- Motivating gentle exercise in high-risk, low-mobility patients
- Real-time biometrics to ensure exertion remains within safe bounds
- Scalability for hospital or home-based use

## Getting Started

### Hardware Requirements
- Arduino Nano (or compatible)
- Pulse Oximeter Sensor
- MPU6050 Accelerometer
- USB cable

## Software Setup

Follow these steps to set up and run Neuro Nudge locally on your machine:

### 1. Clone the repository

```bash
git clone https://github.com/JeremySiu/neuro-nudge.git
cd neuro-nudge
```

### 2. Set up the Python backend

```bash
cd backend
pip install -r requirements.txt
python app.py
```

Python 3.7 or higher is required.  
(Optional) To use a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Upload Arduino sketch

1. Open `hardware/neuro_nudge.ino` in the Arduino IDE  
2. Connect your Arduino Nano via USB  
3. Select the correct board and port under Tools  
4. Click Upload

### 4. Set up the React frontend

```bash
cd ../frontend
npm install
npm start
```

The game interface will be available at:

```
http://localhost:3000
```

### Optional: Configure serial port

If the backend does not detect your Arduino:

1. Open `backend/app.py`  
2. Update the serial port path (for example, `COM3` on Windows or `/dev/ttyUSB0` on Linux):

```python
ser = serial.Serial('COM3', 9600)
```

You are now ready to run Neuro Nudge.

