# Internet of Things Department Task 2
2nd task of Internet of Things Department - Summer training program at Smart Methods

This Arduino code reads the digital state (HIGH or LOW) of a specific input pin (inPin) and sends the result to the serial monitor at a baud rate of 9600. The setup function initializes the input pin and begins serial communication, while the loop function repeatedly reads the pin state and prints it to the serial monitor every second.

### Tinkercad Link - IOT - Task 2
https://www.tinkercad.com/things/fCKIvsrWkGM?sharecode=xcoOFVMJM0BLbwUjIJvNCnpD6uwHPWZdG4uHolZF8JU

![IOT - Task 2 ](https://github.com/H16Bw/Internet-of-Things-Department-Task-2/assets/139852537/80e688aa-d45c-42cb-a603-fac823c74d09)

## Explanation:

The code defines an integer variable inPin with a value of 4, which represents the number of the input pin that will be used to read the digital state.

In the setup function, pinMode(inPin, INPUT) sets the specified pin (pin 4) as an input, indicating that it will be used to read a digital signal.

The Serial.begin(9600) function initializes the serial communication with the computer at a baud rate of 9600 bits per second.

Inside the loop function, digitalRead(inPin) reads the digital state (either HIGH or LOW) of the input pin, and Serial.print() outputs the result to the serial monitor.

After printing the pin state, delay(1000) is used to pause the execution for 1000 milliseconds (1 second) before starting the next iteration of the loop. This creates a 1-second interval between each pin state reading, allowing us to observe the changes on the serial monitor.
