morse-beacon
============

_morse-beacon_ is a system to convert English text into the Morse code to send
out it by issuing LED blinks and buzzer pings connected to a ESP8266 board.

## Hardware Requirements

* Any ESP8266 board
* 1 Breadboard
* 10 Jumper wires (6 male to male, 4 female to male)
* 1 LED (any color, ~3V, ~5 mA)
* 1 Resistor (330 ohms)
* 1 Buzzer (>= 3.3V)

## Software Requirements

* Arduino IDE `>= 1.8.3`
* Node.js, npm `>= 8.1.3`, `>= 5.0.3`
* Redis `>= 3.2.9`
* Docker, docker-compose `>= 17.06.0`, `>= 1.14.0` (optional)

## Usage

1. Deploy the data collection back end [server](https://github.com/toksaitov/morse-back).

2. Change the beacon [program](https://github.com/toksaitov/morse-beacon)
   sources to point it to the newly deployed back end.

3. Compile and upload the beacon program to the board.

4. Change the client [program](https://github.com/toksaitov/morse-client)
   sources to point it to the same back end.

5. Compile and install the client program program to an Android phone.

6. Send a text message to the server queue through the client program. The board
   will eventually download the message, convert it into the Morse code, and
   play it by issuing LED blinks and buzzer pings.

## Credits

*morse-beacon* was created by [Dmitrii Toksaitov](https://github.com/toksaitov).

