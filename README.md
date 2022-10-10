# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

## Step1:

Initiate the MobileRobot.

## Step2:

Connect your PC with the MobileRobot through WiFi.

## Step3:

Open battery_level.py file and check the battery.

## Step4:

Open the other python files and program the movements of the robot using python.

## Step5:

Execute the python program and record the movements.

## Program:

```python
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    '''
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5]
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second) [0.5,2]
    '''
    ep_led.set_led(comp="all",r=100,g=100,b=0,effect="on")
    
    ep_chassis.move(x=0.7, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=100,g=100,b=0,effect="on")   
    
    ep_chassis.move(x=0, y=0, z=83, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=2.85, y=0, z=0, xy_speed=0.75).wait_for_completed()
    
    ep_chassis.move(x=0, y=0, z=85, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=100,b=100,effect="on")
    
    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on")
    
    ep_led.set_led(comp="all",r=0,g=100,b=100,effect="on")
    ep_chassis.move(x=0, y=0, z=55, xy_speed=1).wait_for_completed()
    
    ep_chassis.move(x=3, y=0, z=0, xy_speed=0.75).wait_for_completed()
    
    ep_chassis.drive_speed(x=0.5,y=0,z=-20)
    time.sleep(14)
    ep_chassis.drive_speed(x=0,y=0,z=0)
    
    ep_robot.close()
    
```

## MobileRobot Movement Image:

## Initial position:

![3da455f5-37cb-4534-8edb-79a445f7d49e](https://user-images.githubusercontent.com/113497340/194830652-f808ca35-8b0d-4e45-a613-8b5883a38456.jpeg)

## Final position:

![e50e36a8-fab4-4c4c-9eb5-0fb922afc386](https://user-images.githubusercontent.com/113497340/194830729-5d2ad62b-c166-48e6-ba42-69c8441393fa.jpeg)



<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:



https://www.youtube.com/shorts/t8nVyGZvT7w

<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
