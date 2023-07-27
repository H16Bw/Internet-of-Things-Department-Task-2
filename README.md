# Internet of Things Department Task 2
2nd task of Internet of Things Department - Summer training program at Smart Methods

This Arduino code reads the digital state (HIGH or LOW) of a specific input pin (inPin) and sends the result to the serial monitor at a baud rate of 9600. The setup function initializes the input pin and begins serial communication, while the loop function repeatedly reads the pin state and prints it to the serial monitor every second.

### Tinkercad Link - IOT - Task 2
https://www.tinkercad.com/things/fCKIvsrWkGM?sharecode=xcoOFVMJM0BLbwUjIJvNCnpD6uwHPWZdG4uHolZF8JU

![‏‏Arduine Transmit code ](https://github.com/H16Bw/Internet-of-Things-Department-Task-2/assets/139852537/82e543af-307d-42d0-9efc-b74e572511b5)

## Arduine Transmit code 

### Explanation:

1. The code defines an integer variable inPin with a value of 4, which represents the number of the input pin that will be used to read the digital state.

2. In the setup function, pinMode(inPin, INPUT) sets the specified pin (pin 4) as an input, indicating that it will be used to read a digital signal.

3. The Serial.begin(9600) function initializes the serial communication with the computer at a baud rate of 9600 bits per second.

4. Inside the loop function, digitalRead(inPin) reads the digital state (either HIGH or LOW) of the input pin, and Serial.print() outputs the result to the serial monitor.

5. After printing the pin state, delay(1000) is used to pause the execution for 1000 milliseconds (1 second) before starting the next iteration of the loop. This creates a 1-second interval between each pin state reading, allowing us to observe the changes on the serial monitor.

## Arduine Receive code 

### Explanation:

1. The code defines an integer constant OUT_PIN with a value of 2, representing the number of the output pin that will be used to control the ON/OFF state.

2. In the setup function, pinMode(OUT_PIN, OUTPUT) sets the specified pin (pin 2) as an output, indicating that it will be used to control the ON/OFF state of the output.
Serial communication with the computer is started using Serial.begin(9600) at a baud rate of 9600 bits per second.

3. Inside the loop function: The program checks if there is data available to read from the Serial Monitor using Serial.available(). If there is data available, it reads the first bit of the received data using bitRead(Serial.read(), 0) and assigns the read state to the variable buttonState.

4. The specified pin (OUT_PIN) is set according to the value of buttonState using digitalWrite(OUT_PIN, buttonState). This means that the button state will control the ON/OFF state of the output pin.

5. The program introduces a delay of 1000 milliseconds (1 second) using delay(1000) before starting the next iteration of the loop. This creates a 1-second interval between each button state reading, allowing us to observe the changes on the Serial Monitor.
