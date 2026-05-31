# IoT LED Control Using Blynk and ESP32

## Overview

This project demonstrates how to control an LED remotely using the Blynk IoT platform and an ESP32 microcontroller. The ESP32 connects to a Wi-Fi network and receives commands from the Blynk mobile application to turn an LED ON or OFF.

## Features

* Remote LED control using the Blynk mobile app
* ESP32 Wi-Fi connectivity
* Real-time ON/OFF switching
* Serial Monitor output for debugging

## Components Required

* ESP32 Development Board
* LED
* 220Ω Resistor
* Breadboard
* Jumper Wires
* Smartphone with Blynk App
* Wi-Fi Connection

## Circuit Connection

| Component       | ESP32 Pin                   |
| --------------- | --------------------------- |
| LED Anode (+)   | GPIO 2                      |
| LED Cathode (-) | GND (through 220Ω resistor) |

## Software Requirements

* Arduino IDE
* ESP32 Board Package
* Blynk Library

## Working Principle

1. The ESP32 connects to the configured Wi-Fi network.
2. The ESP32 connects to the Blynk Cloud using the Authentication Token.
3. A Button Widget in the Blynk app is linked to Virtual Pin V0.
4. When the button is pressed, Blynk sends the value to the ESP32.
5. The ESP32 turns the LED ON or OFF based on the received value.

## Code Functionality

* `BLYNK_WRITE(V0)` receives button values from the Blynk app.
* `digitalWrite(LED_PIN, state)` controls the LED state.
* `Blynk.run()` maintains communication with the Blynk server.

## Output

The LED connected to GPIO 2 can be controlled remotely through the Blynk mobile application over the Internet.

## Author

Manimaran
