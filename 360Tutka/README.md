# Arduino Radar System with SMS Alerts
By Johannes Päivärinta, Ville Niemi, Jere Siermala and Janne Pauna

This is an Arduino-based radar system that uses two ultrasonic sensors and a SIM900 module to 
detect objects within a certain range and alert the user via SMS if an object 
is detected. The system also includes a servo motor that rotates the sensors to 
scan a wider area. The code is written in C++ and requires the Servo and 
SoftwareSerial libraries to be installed in the Arduino IDE.

## Installation
Install the latest version of the Arduino IDE.
Clone or download the repository to your local machine.
Open the 360Tutka.ino file in the Arduino IDE.
Connect your Arduino board to your computer via USB cable.
Select the correct board and serial port in the Arduino IDE.
Upload the code to the Arduino board.

## Configuration
Connect two ultrasonic sensors to the Arduino board as follows:
* HC-SR04 Sensor 1:
  * Connect the Trig pin to pin 10 of the Arduino board.
  * Connect the Echo pin to pin 9 of the Arduino board.
* HC-SR04 Sensor 2:
  * Connect the Trig pin to pin 13 of the Arduino board.
  * Connect the Echo pin to pin 12 of the Arduino board.
* Connect a servo motor to the Arduino board as follows:
  * Connect the signal pin to pin 6 of the Arduino board.
  * Connect the power and ground pins to the corresponding pins on the board.
* Connect a button to the Arduino board as follows:
  * Connect one pin of the button to pin 11 of the Arduino board.
  * Connect the other pin of the button to GND on the board.
* Connect an LED to the Arduino board as follows:
  * Connect the positive pin of the LED to pin 5 of the Arduino board.
  * Connect the negative pin of the LED to GND on the board.
* Insert a SIM card into the SIM900 module and connect it to the Arduino board as follows:
  * Connect the TX pin of the module to pin 7 of the Arduino board.
  * Connect the RX pin of the module to pin 8 of the Arduino board.
* Connect the GND and VCC pins of the module to the corresponding pins on the board.
* Configure the SIM900 module to work with your network provider by following the instructions in the SIM900 documentation.
* Set up the phone number and message text for the SMS alert by modifying the sendSMS() function in the code.

## Usage
Power on the Arduino board and wait for it to 
initialize. Press the button to start the scanning process.
The servo motor will rotate the sensors to 
scan a 180-degree area in front of the board.
If an object is detected within 10 cm of either 
sensor, the LED will blink and an SMS alert will
be sent to the specified phone number. The scanning 
process will stop automatically after a complete scan or 
if the button is pressed again.

## Contributing
If you find any issues or have suggestions for improvement, please submit an issue or pull request on GitHub.
