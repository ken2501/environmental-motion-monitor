# Devlog 00 — Project Planning & Initial Setup

## Goals
- Set up project repository and development structure
- Define initial project scope and system architecture
- Prepare Arduino and Python development environments
- Research sensor options and finalize initial hardware list
- Test serial communication between Arduino and Python

---

## Work Completed
- Created GitHub repository and organized initial folder structure
- Installed Arduino IDE and required Python libraries
- Selected Arduino Nano as the primary microcontroller platform

---

## Work Remaining
- Research telemetry system architecture in greater detail
- Finalize sensor selection
- Test USB serial communication using Python and pyserial
- Define telemetry packet structure

---

## Technical Details

### Planned System Architecture
Sensors → Arduino Nano → Serial USB → Python Backend → Dashboard

### Initial Telemetry Strategy
- Arduino collects sensor readings
- Sensor data transmitted as structured CSV packets
- Python backend parses incoming serial stream
- Dashboard visualizes telemetry data in real time

### Proposed Packet Format
TIME,AX,AY,AZ,TEMP,HUM

### Initial Hardware
- Arduino Nano
- Laptop
- Serial USB

---

## Problems Encountered
No major technical issues encountered at this stage.

---

## Design Decisions (Planned)
- Use serial communication at 115200 baud rate
- Use CSV packet formatting initially to reduce parsing complexity and transmission overhead compared to JSON

---

## Current Status
- Repository and development environment initialized
- Core project direction defined
- Serial communication not yet tested
- Hardware integration not yet started

---

## Next Steps
- Interface MPU6050 sensor
- Acquire accelerometer and gyroscope data
- Implement structured telemetry packets
- Develop initial Python serial parser