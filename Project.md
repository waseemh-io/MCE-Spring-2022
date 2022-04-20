# Project DUE MAY 13th

NOTES:
https://github.com/waseemh-io/MRF-SDN/tree/master/ROS-Introduction-and-Examples

Each group is responsible for creating a powerpoint presentation and recorded video giving a basic introduction to ROS and showing your code for achieving the task below. You must give a code walk through and also run your code to see that you have accomplished the task. All students should take part in the presentation. I would recommend going onto a zoom/google meet up and record yourself while sharing your screen.

### Group 1:
#### Mina, Josiah and Delano

Create a ROS node that reads the keypad from the user and moves the robot in the direction which the user entails. If the robot is ever approaching a wall or boundary, the robot should not hit the wall and instead turn 90 degrees.

- Left key would turn the robot to the left by a certain amount of degrees
- Right key would turn the robot to the right by a certain amount of degrees
- Forward key would move the robot in the forward direction
- Back key would move the robot in the backwards direction

HINT: The walls of the screen are constant. 

### Group 2:

#### Isa, Joseph, Jo

Create a ROS node that asks the user to pick between “1, 2, 3, 4”. Based on what the user selects, the robot is responsible for drawing the pattern of the number they selected.

HINT: Think of the direction which the robot should be facing and moving towards before moving

### Group 3:

#### Daniel, Kevin, Rebecca

Create a ROS node that spawns up 4 robots.

Hint: `roservice call /spawn...`

Each robot can only move in 1 direction. Create a square with all 4 robots.

### Group 4:

#### Christian, Kirill, Tatiana, Alanke

Create a ROS node that spawns up 3 robots next to 1 another (give them some space).

This node should randomly move the first robot (in the line) and have the other two robots follow.
HINT: There are multiple ways to solve this: The commands that you are sending to the first robot, you can also send the same commands to the second and third
OR the second and third robot subscribes to the first robots position and moves accordingly 
