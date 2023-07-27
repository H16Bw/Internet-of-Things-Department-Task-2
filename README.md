# Internet of Things Department Task 2
2nd task of Internet of Things Department - Summer training program at Smart Methods


### Tinkercad Link - IOT - Task 2
https://www.tinkercad.com/things/fCKIvsrWkGM?sharecode=xcoOFVMJM0BLbwUjIJvNCnpD6uwHPWZdG4uHolZF8JU

## Arduine Transmit code 
This Arduino code reads the digital state (HIGH or LOW) of a specific input pin (inPin) and sends the result to the serial monitor at a baud rate of 9600. The setup function initializes the input pin and begins serial communication, while the loop function repeatedly reads the pin state and prints it to the serial monitor every second.

![‏‏Arduine Transmit code ](https://github.com/H16Bw/Internet-of-Things-Department-Task-2/assets/139852537/82e543af-307d-42d0-9efc-b74e572511b5)


### Explanation:

1. The code defines an integer variable "inPin" with a value of 4, which represents the number of the input pin that will be used to read the digital state.

2. In the setup function, "pinMode(inPin, INPUT)" sets the specified pin (pin 4) as an input, indicating that it will be used to read a digital signal.

3. The "Serial.begin(9600)" function initializes the serial communication with the computer at a baud rate of 9600 bits per second.

4. Inside the loop function, "digitalRead(inPin)" reads the digital state (either HIGH or LOW) of the input pin, and "Serial.print()" outputs the result to the serial monitor.

5. After printing the pin state, "delay(1000)" is used to pause the execution for 1000 milliseconds (1 second) before starting the next iteration of the loop. This creates a 1-second interval between each pin state reading, allowing us to observe the changes on the serial monitor.

   

## Arduine Receive code 

This Arduino code converts a digital signal received through the serial input (Serial) into a digital signal on a specified output pin (OUT_PIN). When data is received from the serial input, the code reads the least significant bit (LSB) from the received data and then turns the specified output pin ON or OFF based on the read value.


![Arduine Receive code ](https://github.com/H16Bw/Internet-of-Things-Department-Task-2/assets/139852537/cb33d084-cb6b-4d5f-af15-1aaa9072c2e5)


### Explanation:


1. The code defines an integer variable "OUT_PIN" with a value of 6, which represents the number of the pin used as an output to send a digital signal.
2. In the setup function, "pinMode(OUT_PIN, OUTPUT)" sets the specified pin (pin 6) as an output, indicating that it will be used to send a digital signal.
3. The "Serial.begin(9600)" function initializes the serial communication with the computer at a baud rate of 9600 bits per second.

4. Inside the loop function, "if (Serial.available() == 1)" checks if there is data available on the serial input.

5. If data is available, "Serial.read()" reads the received data from the serial input, and "bitRead()" extracts the least significant bit (LSB) from it and stores it in the "buttonState" variable.

6. The digital signal stored in "buttonState" is then sent to the specified output pin using "digitalWrite(OUT_PIN, buttonState)".

7. "delay(1000)" is used to pause the execution for 1000 milliseconds (1 second) between each reading and sending of the digital signal. This creates a 1-second interval between each operation, allowing for proper signal handling.
