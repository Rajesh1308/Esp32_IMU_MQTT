# ESP32 MQTT Publisher

This project demonstrates how to use an ESP32 microcontroller to publish data to an MQTT server. The ESP32 connects to a Wi-Fi network and sends sensor data (e.g., temperature, humidity, or any other data) to a specified MQTT topic at regular intervals.

## Features

- Connects to a Wi-Fi network.
- Publishes data to an MQTT broker using the Paho MQTT library.
- Supports secure connections using TLS (if configured).
- Configurable publish interval for sending data.

## Requirements

- ESP32 development board.
- Arduino IDE or PlatformIO for programming the ESP32.
- PubSubClient library for MQTT communication.

## Installation

1. Install the Arduino IDE or PlatformIO.
2. Install the PubSubClient library:
   - In Arduino IDE, go to **Sketch** > **Include Library** > **Manage Libraries** and search for "PubSubClient" to install it.
3. Clone this repository or create a new sketch in the Arduino IDE.

## Code Overview

The code typically includes the following steps:

1. **Include Libraries**: Import necessary libraries for Wi-Fi and MQTT.
2. **Define Wi-Fi and MQTT Credentials**: Set up your Wi-Fi SSID, password, MQTT broker address, and topic.
3. **Connect to Wi-Fi**: Use the `WiFi.begin()` method to connect to the specified Wi-Fi network.
4. **Set Up MQTT Client**: Initialize the MQTT client and set the server address and port.
5. **Publish Data**: In the `loop()` function, read sensor data and publish it to the MQTT topic using `client.publish()`.
6. **Maintain Connection**: Ensure the MQTT connection is maintained by calling `client.loop()`.

## Usage

1. Update the Wi-Fi credentials and MQTT broker details in the code.
2. Upload the code to your ESP32 board using the Arduino IDE.
3. Open the Serial Monitor to view connection status and published data.

## License

This project is licensed under the MIT License.
