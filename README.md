## robot motion 
This repository contains a Python script for controlling the motion of a bipedal robot using six servo motors (three for each leg).

## description
The script defines the servo motor positions for the right and left legs, and then moves the legs through a basic walking cycle

## Algorthim
right_leg_motors = [servo_right_thigh, servo_right_knee, servo_right_ankle]
left_leg_motors = [servo_left_thigh, servo_left_knee, servo_left_ankle]

for motor in right_leg_motors:
    motor.angle = 90
for motor in left_leg_motors:
    motor.angle = 90

right_leg_motors[0].angle = 120
right_leg_motors[1].angle = 60
right_leg_motors[2].angle = 120

left_leg_motors[0].angle = 60
left_leg_motors[1].angle = 120
left_leg_motors[2].angle = 60

time.sleep(1)

for motor in right_leg_motors:
    motor.angle = 90
for motor in left_leg_motors:
    motor.angle = 90

## explanation
`right_leg_motors`: containing 3 motors for the right leg.

 `left_leg_motors`: containing 3 motors for the left leg.
 
 First, a loop sets the angle of each motor in both lists to 90 degrees.

 right leg
The first motor in the right leg is set to 120 degrees.
The second motor in the right leg is set to 60 degrees.
The third motor in the right leg is set to 120 degrees.

left leg 
The first motor in the left leg is set to 60 degrees.
The second motor in the left leg is set to 120 degrees.
The third motor in the left leg is set to 60 degrees.

After that, the code pauses for 1 second.

two more loops set the angle of each motor back to 90 degrees.
