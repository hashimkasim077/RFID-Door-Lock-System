# RFID Door Lock System

A simple RFID-based door lock using Arduino and Servo motor.  
Unlocks the door when an authorized RFID card is scanned.

## Project Overview

Basic access control system:  
RFID reader (RC522) scans card → Arduino checks UID → Servo unlocks door if authorized.

Common uses:
- Smart homes
- Office access control
- School labs
- Secure cabinets

## Components

- Arduino UNO
- RFID Reader (RC522)
- RFID Card / Tag
- Servo Motor (e.g. SG90)
- Jumper wires

## Pin Connections

**RFID RC522 → Arduino**

| RC522 Pin | Arduino Pin |
|-----------|-------------|
| SDA       | D10         |
| SCK       | D13         |
| MOSI      | D11         |
| MISO      | D12         |
| RST       | D9          |
| 3.3V      | 3.3V        |
| GND       | GND         |

**Servo → Arduino**

| Servo Wire | Arduino Pin |
|------------|-------------|
| VCC        | 5V          |
| GND        | GND         |
| Signal     | D6          |

## How It Works

1. RFID reader waits for card  
2. Card scanned → UID read  
3. Arduino compares UID with stored value  
4. Match → Servo rotates to unlock (90°)  
5. After 3 seconds → Servo returns to lock (0°)

## Project Logic

Scan RFID Card
↓
Read UID
↓
Compare with authorized UID
┌───────────────┐
│               │
Match?   No    Yes
│               │
Keep locked    Unlock


## Applications

- Smart door locks
- RFID access systems
- School / office entry
- IoT security prototypes

## Future Improvements

- Add green/red LEDs
- Buzzer for feedback
- Multiple card support
- ESP32 + WiFi control
- Mobile app integration

