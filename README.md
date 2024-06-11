Hand Gesture Controlled UAV

This project involves creating a hand gesture-controlled UAV (Unmanned Aerial Vehicle) using an ESP8266, MPU6050 sensor, and NRF24L01 modules. The UAV's flight control is managed by interpreting the angles measured by the MPU6050 and transmitting this data wirelessly to the UAV, which adjusts its flight surfaces accordingly. The throttle control is managed via a switch mechanism on the transmitter.
Table of Contents

    Introduction
    Components
    Circuit Diagram
    Setup and Configuration
    Code
    Usage
    Troubleshooting
    Contributing
    License

Introduction

This project aims to build a UAV controlled by hand gestures. The MPU6050 sensor captures hand movements and translates them into angles, which are then sent via the NRF24L01 modules to the UAV. The UAV responds by adjusting its elevator, rudder, and ailerons using servo motors. The throttle is controlled via a switch on the transmitter.
Components

    ESP8266 (x2): Microcontroller for handling data processing and communication.
    MPU6050: Sensor for measuring angles.
    NRF24L01 (x2): Wireless modules for data transmission between the transmitter and receiver.
    Servo Motors (x3): For controlling the elevator, rudder, and ailerons.
    Switch: For throttle control.
    Power Supply: Appropriate power sources for ESP8266, servos, and other components.
    Miscellaneous: Wires, breadboard, connectors, etc.

Setup and Configuration

    Install Arduino IDE: Download and install the Arduino IDE from Arduino's official website.
    Install ESP8266 Board: In Arduino IDE, go to File > Preferences. In the Additional Boards Manager URLs field, add http://arduino.esp8266.com/stable/package_esp8266com_index.json. Then go to Tools > Board > Boards Manager, search for "esp8266", and install it.
    Install Libraries:
        MPU6050: Install via Library Manager (search for "MPU6050").
        RF24: Install via Library Manager (search for "RF24").
        Servo: Install via Library Manager (search for "Servo").

Code

    Transmitter Code: The transmitter code will initialize the MPU6050, read the angles, and send this data through the NRF24L01.
    Receiver Code: The receiver code will read the data from the NRF24L01 and control the servos based on the received angles.

Usage

    Power Up: Ensure both the transmitter and receiver are powered up.
    Calibrate: Place the MPU6050 in a stable position and ensure it initializes correctly.
    Operate: Use hand gestures to control the UAV. The transmitter will send angle data to the receiver, which will adjust the servos accordingly. Use the switch to control the throttle.

Troubleshooting

    No Data Transmission: Check connections of the NRF24L01 modules and ensure they are properly powered.
    Servo Not Moving: Verify the servo connections and ensure they are receiving the correct signals.
    Incorrect Angles: Calibrate the MPU6050 sensor and ensure it is correctly positioned.

Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any bugs or feature requests.
