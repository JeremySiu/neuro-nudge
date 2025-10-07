# Neuro Nudge

A rhythm-based therapeutic game that promotes physical activity and monitors heart rate in bedridden delirium patients.

![NeuroNudge](https://github.com/user-attachments/assets/df003e0b-5dd6-4237-8de8-1ce3d1b54ee6)

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
![SetupImage1](https://github.com/user-attachments/assets/d6fc917b-3c0c-4e13-8675-50c583368a11)
![SetupImage2](https://github.com/user-attachments/assets/d5342e19-a94d-4b31-a144-a1ebbd1a1211)

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

