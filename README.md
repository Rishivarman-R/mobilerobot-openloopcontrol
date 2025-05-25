# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure
Step 1: Use from robomaster import robot<br>
Step 2: Choose the x,y,z - axis movement distance(meters).<br>
Step 3: Give ep_chasis.move to move straight<br>
Step 4: Give ep_chasis.drive to get circular motion.<br>
Step 5: Give ep_chasis.move to move straight<br>
Step 6: Give ep_chasis.drive to get circular motion.<br>


## Program
```
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis

    # Movement sequence
    ep_chassis.move(x=-1, y=0, z=-8, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-135, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=1, y=0.8, z=0, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=135, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=1, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=1, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-150, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=1, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=150, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=1, y=0, z=8, xy_speed=0.65).wait_for_completed()

    # Drive with speed control
    ep_chassis.drive_speed(x=0.2, y=0, z=-20)
    time.sleep(15)

    # Close connection
    ep_robot.close()

```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here


<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here
<br>
<br>
file:///C:/Users/admin/Documents/MY%20PERSONAL%20GALLERY/mobile%20robotic.mp4

<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
