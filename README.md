# RFID Door Lock with Servo (Arduino)

A simple **RFID-based smart door lock** built using **Arduino, RC522 RFID reader, and a Servo motor**.
The system unlocks the door when an **authorized RFID card** is scanned.

---

## Project Overview

This project demonstrates a **basic access control system**.
When a valid RFID card is placed near the reader, Arduino verifies the card ID and rotates the servo motor to unlock the door.

After a few seconds, the servo returns to its original position to lock the door again.

---

## Features

* RFID-based authentication
* Automatic door unlock using servo
* Simple and lightweight code
* Easy to modify for multiple RFID cards
* Suitable for learning **IoT and embedded systems**

---

## Components Used

* Arduino UNO
* RC522 RFID Reader
* RFID Card / Tag
* Servo Motor (SG90)
* Jumper Wires
* Breadboard

---

## Pin Configuration

| Component    | Arduino Pin |
| ------------ | ----------- |
| RFID SDA     | D10         |
| RFID SCK     | D13         |
| RFID MOSI    | D11         |
| RFID MISO    | D12         |
| RFID RST     | D9          |
| Servo Signal | D6          |
| RFID VCC     | 3.3V        |
| GND          | GND         |

---

## How It Works

1. The RFID reader scans the card.
2. Arduino reads the **UID (Unique ID)** of the card.
3. The UID is compared with the stored authorized UID.
4. If the UID matches:

   * The servo rotates to **unlock the door**.
5. After a few seconds:

   * The servo rotates back to **lock the door**.

---

## Getting the RFID Card UID

Upload a simple RFID reader code and open the **Serial Monitor**.
When a card is scanned, the UID will appear like this:

```
Card UID: 3A 7F B2 11
```

Add it to the program:

```
byte allowedUID[4] = {0x3A, 0x7F, 0xB2, 0x11};
```

---

## Applications

* Smart home door lock
* Office access control
* School or lab entry system
* Arduino learning projects

---

## Future Improvements

* Add **LED and buzzer indicators**
* Store **multiple RFID cards**
* Use **ESP32 for WiFi-based access logs**
* Create a **mobile app control system**

---

## License

This project is open-source and free to use for learning and educational purposes.
