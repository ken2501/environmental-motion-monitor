# Environmental Motion Monitor

## Overview
A real-time telemetry system using an Arduino Nano, motion sensing, and environmental sensors to collect, process, and visualizs

## Goals
- Learn embedded systems fundamentals
- Interface real-world sensors
- Build telemetry pipelines
- Visualize live sensor data on PC
- Practice engineering documentation

## Planned Features
- Motion and orientation tracking
- Environmental monitoring
- Live serial telemetry
- Real-time Python dashboard visualization
- Telemetry data logging    

## Planned Development Stages
1. Environment setup and serial communication
2. Sensor integration
3. Structured telemetry packets
4. Python telemetry backend
5. Real-time dashboard visualization
6. Data logging and filtering

## Hardware
- Arduino Nano
- BME280 environmental sensor
- MPU6050 IMU
- Breadboard
- Jumper wires

## Initial Architecture

'''
┌────────────────────────┐
│   Physical Environment │
│                        │   
│ - Motion               │
│ - Vibration            │ 
│ - Temperature          │
│ - Humidity             │
└──────────┬─────────────┘
           │
           ▼
┌──────────────────────────┐
│       Sensors            │ 
│                          │ 
│ - MPU6050 (IMU)          │
│ - BME280 (Environmental) │
└──────────┬───────────────┘
           │
           │ I2C Communication
           ▼
┌─────────────────────────────────┐
│    Arduino Nano                 │
│                                 │
│ Responsibilities:               │
│ - Read sensor data              │
│ - Manage sampling timing        │ 
│ - Package telemetry             │ 
│ - Send serial packets           │
│ - Perform lightweight filtering │
└──────────┬──────────────────────┘
           │
           │ USB Serial (115200 baud)
           ▼
┌───────────────────────────────┐
│   Python Backend              │             
│                               │
│ Responsibilities:             │
│ - Read serial stream          │
│ - Validate telemetry packets  │
│ - Parse sensor data           │
│ - Maintain data buffers       │
│ - Log telemetry data          │
└──────────┬────────────────────┘
           │
           ├──────────────┐
           │              │
           ▼              ▼
┌────────────────┐   ┌────────────────┐
│ Live Dashboard │   │ Data Logging   │
│                │   │                │
│ - Real-time    │   │ - CSV storage  │
│   graphs       │   │ - Historical   │
│ - System       │   │   telemetry    │
│   status       │   │ - Session data │
│ - Telemetry    │   │                │
│   monitoring   │   │                │
└────────────────┘   └────────────────┘
'''
## Project Status
Planning phase
