
<img width="3188" height="1202" alt="frame (3)" src="https://github.com/user-attachments/assets/517ad8e9-ad22-457d-9538-a9e62d137cd7" />


# PASU🎯


## Basic Details
### Team Name: Pasu_Labs


### Team Members
- Team Lead: MADHAV K ANIL - MA COLLEGE OF ENGINEERING, KOTHAMANGALAM
- Member 2: KALYANI B - MA COLLEGE OF ENGINEERING, KOTHAMANGALAM

### Project Description
'PASU' is a mobile, character-driven dustbin on wheels that hates doing its job. Controlled manually, it reacts dramatically whenever someone tries to throw waste inside. With iconic Malayalam dialogue and runaway antics, it turns a boring bin into the sassiest gadget in the room.

### The Problem (that doesn't exist)
In a world where dustbins silently suffer in dignity, no one cares about their feelings as they’re forced to swallow our garbage every day.

### The Solution (that nobody asked for)
Introducing Moody Bin —a runaway, wheeled dustbin with a dramatic personality. Pour waste in, and instead of accepting it quietly, he speaks up for himself, and might even roll away in protest.

## Technical Details

### Technologies/Components Used
For Software:
- Sensecarft AI 
- ARDUINO IDE
- FUSION 360


For Hardware:
- ESP 32
- GROOVE VISION AI V2  
- FN-M16P( MP3 audio module)
- 3W Speaker
- Li ion Batttery
- Dust bin
- Foam board
- Jumper wires

### Implementation
For Software:
Wi-Fi Manual Control (Mobile App):
An app connects to the ESP32 over Wi-Fi.
App has directional buttons (Forward, Backward, Left, Right, Stop) to control the bin’s motor driver via ESP32 GPIO pins.
Commands are sent as HTTP requests or via WebSocket for smoother control.

Waste Detection Trigger (Groove Vision AI Camera):
The Groove Vision AI V2 Camera is trained (custom ML model) to recognize “waste items” using a small dataset.
When the camera detects waste entering the bin, it sends a digital signal to the ESP32 
ESP32 processes the detection event and triggers the “reaction” sequence.

Audio Playback (ESP32 + FN-M16P or DFPlayer Mini):
ESP32 sends serial commands to the audio module to play a Malayalam meme dialogue.
Audio files are stored on the module’s SD card.
A simple random number generator in ESP32 code picks which file to play for each detection.

# Installation
Hardware Setup

Wi-Fi Manual Control
ESP32 programmed to receive commands from a mobile app over Wi-Fi.
App sends movement commands (Forward, Backward, Left, Right, Stop) to control the motor driver connected to the wheels.

Waste Detection (Groove Vision AI Camera):
Groove Vision AI V2 Camera trained using a custom ML model to detect waste items.
When waste is detected, the camera sends a signal to the ESP32.

Reaction Sequence:
On detection, ESP32 triggers the audio module (FN-M16P / DFPlayer Mini) to play a random Malayalam meme dialogue stored on its SD card.

System Flow:
User controls movement via mobile app → ESP32 drives wheels.
Waste enters bin → Camera detects → ESP32 plays dialogue through speakers.


# Run
Run
Power On:
Switch on the ESP32-based control system and the Groove Vision AI Camera.
Ensure the audio module SD card is inserted with the dialogue files.

Connect:
Connect your mobile device to the same Wi-Fi networK as the bin.

Control Movement:
Use the app’s directional buttons to move the bin (Forward, Backward, Left, Right, Stop).

Trigger Reaction:
Drop waste into the bin.
Groove Vision AI Camera detects waste → sends signal to ESP32 → plays a random Malayalam meme dialogue through the speaker.

### Project Documentation

Software Documentation – Moody Bin
Overview
The software for Moody Bin enables Wi-Fi-based manual control and AI-powered waste detection. A Flutter mobile app communicates with the ESP32 over Wi-Fi to move the bin. The Groove Vision AI Camera, trained with a custom ML model, detects waste items and signals the ESP32 to trigger audio playback of random Malayalam meme dialogues via an audio module.

Implementation:
Wi-Fi Manual Control (Flutter App → ESP32)
The Flutter app sends directional commands (Forward, Backward, Left, Right, Stop) over Wi-Fi.
ESP32 processes these commands and controls the motor driver connected to the wheels.

Waste Detection (Groove Vision AI Camera):
Trained using SenseCraft ML tool with a small dataset of waste images
On detection, the camera sends a signal to the ESP32 via UART/I2C.
Audio Reaction (ESP32 + FN-M16P / DFPlayer Mini)
ESP32 triggers the audio module to play one malayalam dialogue,

Tools & Libraries
Software: Arduino IDE, Flutter SDK, SenseCraft ML Tool.
Libraries: WiFi.h, ESPAsyncWebServer, SoftwareSerial.

# Screenshots (Add at least 3)
<img width="1881" height="886" alt="image" src="https://github.com/user-attachments/assets/46628790-177b-4a54-86cc-e3c769308ff9" />
SENSECRAFT AI ML TRAINING
![WhatsApp Image 2025-08-09 at 05 39 42_8c2937d0](https://github.com/user-attachments/assets/65c46ba7-8693-4f97-beae-9cd7b1164114)
GROVE VISION AI VE CAMERA IMPLEMENTATION

# Diagrams
[ESPP8266 App]  <--Wi-Fi-->  [ESP32]
                                 |\
                                 | \__ Motor Driver --> Left Motor (Wheel)
                                 | /                --> Right Motor (Wheel)
                                 |/
                 [Groove Vision AI Camera]  ->(serial/signal)-> ESP32
                                 |
                                 v
                           (detects waste)

                        [ESP32] --serial--> [Audio Module (DFPlayer / FN-M16P)] -> Speaker

Power sources: Battery (motor supply) ---- Motor Driver VIN
               5V regulator / Battery 5V -> ESP32 VIN (or 5V regulator) + Audio Module 5V
               All GNDs tied together


# Schematic & Circuit
![WhatsApp Image 2025-08-09 at 05 09 47_0bfd4c33](https://github.com/user-attachments/assets/922a064e-7cfa-4268-b681-2369df166ef4)


# Build Photos and
# PROJECT DEMO Video
https://drive.google.com/drive/folders/1wuGUb5AkMFYW9BUc2J1pq5HgqjszH769?usp=sharing
(please open the drive)


## Team Contributions
MADHAV K ANIL: HARDWARE, ML TRAINING, DESIGN
KALYANI: SOFTWARE, DESIGN

---
Made with ❤️ at TinkerHub Useless Projects 

![Static Badge](https://img.shields.io/badge/TinkerHub-24?color=%23000000&link=https%3A%2F%2Fwww.tinkerhub.org%2F)
![Static Badge](https://img.shields.io/badge/UselessProjects--25-25?link=https%3A%2F%2Fwww.tinkerhub.org%2Fevents%2FQ2Q1TQKX6Q%2FUseless%2520Projects)


