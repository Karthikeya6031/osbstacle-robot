# Obstacle Avoiding Robot

This Arduino sketch implements the code for an obstacle avoiding robot using an Arduino board, an ultrasonic sensor, servo motor, and motor driver.

## Components Used
- Arduino board (e.g., Arduino Uno)
- L298N motor driver module
- HC-SR04 ultrasonic sensor
- SG90 servo motor
- DC motors and wheels for movement

## Libraries Required
- Servo.h: Standard Arduino library for controlling servo motors.
- NewPing.h: Library for interfacing with ultrasonic sensors.

## Pin Connections
- *Motor Driver (L298N)*
  - LeftMotorForward: Pin 4
  - LeftMotorBackward: Pin 5
  - RightMotorForward: Pin 6
  - RightMotorBackward: Pin 7
- *Ultrasonic Sensor (HC-SR04)*
  - trig_pin: Analog pin A1
  - echo_pin: Analog pin A2
- *Servo Motor (SG90)*
  - Signal pin: Pin 10

## Operation
1. The sketch initializes the pin modes for motor control, ultrasonic sensor, and servo motor.
2. The servo motor rotates to scan for obstacles on both the left and right sides.
3. Based on the distance readings from the ultrasonic sensor, the robot decides whether to move forward or change direction to avoid obstacles.
4. If an obstacle is detected within a specified range (30 cm in this case), the robot stops, backs up, and then turns in the direction with more clearance.
5. The robot continuously reads the distance and adjusts its movement accordingly to navigate while avoiding obstacles.

## Notes
- Adjustments to the servo motor's scanning range (50 to 170 degrees) can be made depending on the robot's design and environment.
- The distance threshold for obstacle detection can be modified as per requirements.
- Ensure proper connections and power supply to the components to avoid malfunction or damage.

This code provides a basic framework for building an obstacle avoiding robot. Further enhancements such as PID control, additional sensors, or wireless communication can be implemented for more advanced functionality.

*Author:* Technical Ninja

Feel free to customize and expand upon this code for your specific robot project needs!
