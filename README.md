**General Description:**

This project is designed to function as a proximity detection and warning system using an ultrasonic sensor. When powered on, the system continuously monitors the distance between itself and nearby objects. Based on how close an object is, the device provides feedback using LEDs and a buzzer to indicate safe, cautionary, or dangerous distances. The system updates readings in real time and gives both visual and audible warnings as objects move closer, making it useful for basic obstacle detection or distance monitoring applications.

**Problem to be Solved:**

The goal of this project is to create a simple and effective way to detect how close an object is to a sensor and notify a user when that object becomes too close. This type of system can be used in real-world applications such as parking sensors, collision avoidance systems, or safety devices where maintaining a minimum distance from obstacles is important.

**The Sensors and Attachments:**

The primary sensor used in this project is an ultrasonic sensor, which measures the distance to nearby objects by emitting sound waves and calculating how long it takes for the echo to return. The system also includes three LEDs that act as visual indicators of distance: a green LED to show that an object is at a safe distance, a yellow LED to indicate that an object is approaching, and a red LED to signal that an object is dangerously close. Additionally, a buzzer is included to provide an audible warning when the closest distance threshold is reached, helping ensure that alerts are noticeable even without visual attention.

**Functions of the Device:**

The device continuously measures distance values using the ultrasonic sensor and updates these readings at short time intervals. It processes the distance data and compares it against predefined threshold values to determine the current proximity state. Based on the detected distance, the device activates the appropriate LED and, if necessary, the buzzer. The system ensures that only one state is active at a time, preventing conflicting signals and providing clear feedback to the user.

**Timeline / Outline:**

Set up and test the ultrasonic sensor
Add continuous distance reading and console output
Configure LEDs for visual feedback
Implement distance thresholds for safe, caution, and danger states
Add buzzer activation for the closest distance range
Optimize timing and responsiveness of sensor readings
Test system reliability with moving objects

**Code Description:**

The program begins by importing the necessary pi-top components and a timing function to control the update rate of the system. Hardware components are then assigned to specific digital ports, including the ultrasonic sensor, three LEDs, and a buzzer. Once initialized, the program enters an infinite loop that continuously reads distance values from the ultrasonic sensor and prints them to the console. A short delay is included between readings to maintain stable sensor performance. The measured distance is compared against multiple threshold values, and based on these comparisons, the program turns on the appropriate LED while ensuring the others are turned off. When the distance falls below the minimum threshold, the buzzer is activated along with the red LED to indicate a critical warning state. This loop runs continuously, allowing the system to respond in real time to changes in distance.

**Challenges and Lessons Learned:**

One of the main challenges was determining appropriate distance thresholds that provided clear and reliable feedback without rapidly switching between states. Another challenge involved ensuring that the LEDs and buzzer were properly synchronized so that only the correct indicators were active at any given time. Additionally, working with real-time sensor data required careful timing to avoid unstable or inconsistent readings. Through this project, I gained a better understanding of how ultrasonic sensors operate, how to integrate multiple output devices, and how to structure control logic for real-time embedded systems. I also became more comfortable working with hardware components in Python and organizing a project clearly using GitHub documentation.
