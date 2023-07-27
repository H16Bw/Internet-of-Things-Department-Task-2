# Internet of Things Department Task 2
2nd task of Internet of Things Department - Summer training program at Smart Methods


### Tinkercad Link - IOT - Task 2
https://www.tinkercad.com/things/fCKIvsrWkGM?sharecode=xcoOFVMJM0BLbwUjIJvNCnpD6uwHPWZdG4uHolZF8JU

## Arduine Transmit code 

![‏‏Arduine Transmit code ](https://github.com/H16Bw/Internet-of-Things-Department-Task-2/assets/139852537/82e543af-307d-42d0-9efc-b74e572511b5)

   

## Arduine Receive code 


![Arduine Receive code ](https://github.com/H16Bw/Internet-of-Things-Department-Task-2/assets/139852537/cb33d084-cb6b-4d5f-af15-1aaa9072c2e5)


# Explanation:

This code consists of two devices that work together using Serial Communication. The first device is connected to an input pin (inPin), and the second device is connected to an output pin (OUT_PIN). When the first device reads the state of the input pin and sends it via Serial Communication, the second device reads this state and sends it to the output pin.

## Code for the first device (Transmitter):

- The variable inPin is defined with a value of 4, which represents the number of the input pin.
- In the setup function:
  - pinMode(inPin, INPUT) sets the specified pin (pin 4) as an input.
  - Serial.begin(9600) initiates serial communication with the computer at a baud rate of 9600 bits per second.
- In the loop function:
  - Serial.print(digitalRead(inPin)) reads the digital state (HIGH or LOW) of the input pin and sends it to the Serial Communication.

## Code for the second device (Receiver):

- The variable OUT_PIN is defined with a value of 6, which represents the number of the output pin.
- In the setup function:
  - pinMode(OUT_PIN, OUTPUT) sets the specified pin (pin 6) as an output.
  - Serial.begin(9600) initiates serial communication with the computer at a baud rate of 9600 bits per second.
- In the loop function:
  - If there is data available on the Serial Communication using Serial.available(), the least significant bit (LSB) of the received data is read using bitRead(), and it is stored in the variable buttonState.
  - The digital state stored in buttonState is then sent to the specified output pin as a digital signal using digitalWrite(OUT_PIN, buttonState).
  - A delay of 1000 milliseconds (1 second) is added using delay(1000) between each reading and sending of the digital signal. This creates a time interval between each operation to handle the signals properly.
