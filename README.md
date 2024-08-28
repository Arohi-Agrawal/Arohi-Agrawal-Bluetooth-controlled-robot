# Arohi-Agrawal-Bluetooth-controlled-robot
This project involves designing a versatile Arduino Nano-based mobile robot with wireless control and obstacle detection, exploring its technical aspects, functionality, and future improvements.

Introduction:- 
The increasing demand for automation and remote control has spurred advancements in mobile robotics. This report details the design and development of a Multi-Purpose Mobile Robot with Arduino Nano (MPMC), a versatile robot capable of controlled movement and basic obstacle detection.  This robot utilises an Arduino Nano microcontroller as its central processing unit. The Arduino communicates wirelessly with a user device via a Bluetooth module, enabling remote control of the robot's movement (forward, backward, left, right). Additionally, the MPMC incorporates IR sensors for short-range obstacle detection and an ultrasonic sensor for long-range obstacle detection (depending on the specific design). By combining these components and leveraging the power of Arduino programming, the MPMC robot offers a practical platform for exploring basic mobile robot functionalities. This report delves into the technical details of the MPMC, explaining the function of each component, the overall working principle, and the program that governs the robot's behaviour. We will also explore the limitations of the current design and discuss potential future advancements for this versatile mobile robot.

Working Principle:-
1.User Input: 
  The user sends movement commands (forward, backward, left, right) via Bluetooth to the robot. 
2. Bluetooth Reception:
  The Bluetooth module receives these commands and transmits them as data to the Arduino Nano. 
3. Command Processing:
  The Arduino program interprets the received data, identifying the desired movement direction. 
4. Movement Control: 
   Based on user commands and sensor data  the program generates control signals. These signals, often in the form of Pulse Width Modulation (PWM), are sent to the motor driver (if used) or directly to the 
   motors. 
5. Motor Actuation: 
   The motor driver translates the control signals into appropriate power levels for the DC motors. The motors then rotate accordingly, causing the robot to move in the desired direction. 
6. Continuous Loop: 
   The program continuously loops through these steps, constantly receiving commands, potentially incorporating sensor data, and controlling the robot's movement. This cycle ensures the robot responds to user 
   input and adapts to its environment (if obstacle avoidance is enabled).

Working of Each Block:- 
1. Arduino Nano:
  The brain of the robot, a single-board microcontroller.  It can be programmed using the Arduino IDE to receive commands, interpret them, and control other components.  It has built-in analog and digital pins 
  for connecting sensors and motors (may require additional circuitry for motor control).  It processes sensor data, user commands (via Bluetooth), and sends control signals based on the program. 
2. Bluetooth Module: 
   Enables wireless communication between the robot and a user device (phone, computer) through Bluetooth technology.  It acts as a bridge, receiving commands from the user device and transmitting them to the 
   Arduino for processing.  The program typically includes libraries to handle Bluetooth communication and read incoming data.  
3. IR Sensor(s):  
   Detects nearby objects by emitting and receiving infrared radiation.  Useful for short-range obstacle detection (e.g., detecting walls or objects close to the robot).  The sensor outputs a voltage signal that 
   varies depending on the distance to the object.  The Arduino program reads this voltage and determines if an obstacle is present based on pre-defined thresholds.  
4. Ultrasonic Sensor:  
  Measures distance using sound waves.  Emits a high-frequency sound pulse and measures the time it takes for the echo to return.  This time is converted to distance using the speed of sound.  Useful for long- 
  range obstacle detection, allowing the robot to avoid objects further away than IR sensors can detect.  The Arduino program reads the distance data and adjusts movement based on pre-defined safety zones. 
5. DC Motors (and potentially Motor Driver):
  Provide the driving force for the robot's movement.  May require a separate motor driver circuit if the Arduino cannot directly supply enough current for the motors.  The program sends control signals (pulse 
  width modulation - PWM) to the motor driver, which regulates the speed and direction of the motors. The robot's movement (forward, backward, left, right) depends on the combination of signals sent to each motor.

Limitations and Conclusion:-
1.Sensor range limitations 
2.Environmental factors affecting sensor performance
3.Basic movement control (may lack advanced features) 


Future Scope:- 
1. Implementing line following capabilities 
2.Adding additional sensors for more complex environment interaction 
3.Upgrading to a more powerful microcontroller
4. Developing a mobile app for control 
5.Obstacle avoider
6.Edge detector

