# robot-walking-servo
This repository contains an Arduino project to control servo motors for a quadruped robot walking motion.

## Description

The project uses servo motors to create a walking motion for a quadruped (four-legged) robot. Each leg is equipped with two servo motors: one for the hip joint and one for the knee joint. The code provides a basic algorithm to coordinate the movements of the legs to achieve a walking gait.

## Components

- Arduino board
- 8 Servo motors (2 per leg)
- Quadruped robot frame
- Jumper wires
- Power supply

## Circuit Diagram

(Insert a simple circuit diagram here showing how to connect the servos to the Arduino board.)

## Code

The algorithm is implemented in an Arduino sketch (`robot_walking.ino`). The code initializes eight servo motors and defines their initial positions. It then enters a loop where it alternates the movement of the front and back legs to simulate walking.

### Setup

1. **Attach Servo Motors:**
   Attach each servo motor to the corresponding pin on the Arduino board as defined in the code.

2. **Initial Angles:**
   Set the initial angles for the hip and knee servos to a neutral position (90 degrees).

3. **Walking Cycle:**
   Implement a simple walking cycle that moves the front and back legs in coordination.

### Code Explanation

Here is the Arduino code that controls the walking motion:

```cpp
#include <Servo.h>


Servo hipServo1, kneeServo1; 
Servo hipServo2, kneeServo2; 
Servo hipServo3, kneeServo3; 
Servo hipServo4, kneeServo4; 


const int hipPin1 = 2, kneePin1 = 3;
const int hipPin2 = 4, kneePin2 = 5;
const int hipPin3 = 6, kneePin3 = 7;
const int hipPin4 = 8, kneePin4 = 9;


int initialHipAngle = 90;
int initialKneeAngle = 90;

void setup() {
  
  hipServo1.attach(hipPin1);
  kneeServo1.attach(kneePin1);
  hipServo2.attach(hipPin2);
  kneeServo2.attach(kneePin2);
  hipServo3.attach(hipPin3);
  kneeServo3.attach(kneePin3);
  hipServo4.attach(hipPin4);
  kneeServo4.attach(kneePin4);

  hipServo1.write(initialHipAngle);
  kneeServo1.write(initialKneeAngle);
  hipServo2.write(initialHipAngle);
  kneeServo2.write(initialKneeAngle);
  hipServo3.write(initialHipAngle);
  kneeServo3.write(initialKneeAngle);
  hipServo4.write(initialHipAngle);
  kneeServo4.write(initialKneeAngle);
}

void loop() {
  // Move front legs forward
  hipServo1.write(70);
  hipServo2.write(70);
  delay(500);
  
  hipServo3.write(70);
  hipServo4.write(70);
  delay(500);
  
  
  hipServo1.write(110);
  hipServo2.write(110);
  delay(500);
  

  hipServo3.write(110);
  hipServo4.write(110);
  delay(500);
}
### How to Use

1. **Clone the Repository:**
   ```sh
   git clone https://github.com/USERNAME/robot-walking-servo.git
   cd robot-walking-servo
   ```

2. **Open in Arduino IDE:**
   Open the `robot_walking.ino` file in the Arduino IDE.

3. **Upload the Code:**
   Connect your Arduino board to your computer and upload the code.

4. **Connect Servo Motors:**
   Connect the servo motors to the corresponding pins on the Arduino board as specified in the code.

5. **Power Up:**
   Power up your robot and observe the walking motion.

## Future Improvements

1. **Smooth Movement:**
   Implement smoother transitions between movements to mimic more natural walking.

2. **Sensor Integration:**
   Integrate sensors to adapt the walking motion based on terrain.

3. **Additional Gaits:**
   Implement different walking gaits for various speeds and conditions.

## License

This project is licensed
