# Bluetooth-Controlled Motor Driver

## Overview

This project allows you to control two DC motors using Bluetooth communication. The code is designed for use with an Arduino and an HC-06 Bluetooth module, enabling commands to be sent from a mobile device to control motor directions and speeds.

## Features

- **Bluetooth Control**: Communicates with the HC-06 Bluetooth module to receive commands.
- **Motor Control**: Controls two DC motors with forward, backward, and stop functionalities.
- **Speed Control**: Adjusts motor speed using PWM (Pulse Width Modulation).
- **LED Indicator**: Optionally uses an LED to indicate status.

## Hardware Requirements

- Arduino board (e.g., Arduino Uno)
- HC-06 Bluetooth module
- Two DC motors
- Motor driver circuit (e.g., L298N)
- Connecting wires
- Power supply for motors
- Optional: LED for status indication

## Pin Configuration

- **Motor A**
  - Motor Control Pins: `motorA1` (6), `motorA2` (7)
  - Speed Control Pin: `speedA` (10)
  
- **Motor B**
  - Motor Control Pins: `motorB1` (8), `motorB2` (9)
  - Speed Control Pin: `speedB` (11)

- **LED Pin**: `led` (12)

- **Bluetooth Serial**: RX on pin 4, TX on pin 2

## Installation

1. **Wiring the Hardware**:
   - Connect the HC-06 module to the Arduino (TX to RX and vice versa).
   - Wire the motors to the motor driver according to the driver’s specifications.
   - Connect the motor driver to the Arduino pins as defined above.
   - Connect an LED (optional) to pin 12 for status indication.

2. **Setting Up the Software**:
   - Open the Arduino IDE.
   - Load the provided code.
   - Upload the sketch to your Arduino board.

## Usage

1. Power up the Arduino and Bluetooth module.
2. Pair your mobile device with the HC-06 Bluetooth module.
3. Use a Bluetooth terminal app (like Bluetooth Terminal) to send commands:
   - `1`: Motor A Forward
   - `2`: Motor B Forward
   - `3`: Motor B Backward
   - `4`: Motor A Backward
   - `5`: Motor A Stop
   - `6`: Motor B Stop

The status of each command will be printed to the serial monitor.

## Functions Overview

- `MotorAForward()`: Moves Motor A forward.
- `MotorABackward()`: Moves Motor A backward.
- `MotorAStop()`: Stops Motor A.
- `MotorBForward()`: Moves Motor B forward.
- `MotorBBackward()`: Moves Motor B backward.
- `MotorBStop()`: Stops Motor B.

## Notes

- Ensure that the HC-06 module is configured to the correct baud rate (9600).
- Make sure your power supply is sufficient for the motors.

## Contributing

Contributions are welcome! Feel free to submit pull requests or open issues for suggestions and improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the open-source community for the resources and libraries that made this project possible.

