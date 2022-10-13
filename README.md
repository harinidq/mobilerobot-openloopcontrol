# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:

<br/>Initiate the MobileRobot.


Step2:

<br/>Connect your PC with the MobileRobot through WiFi.

Step3:

<br/>Open battery_level.py file and check the battery.

Step4:

<br/>Open the other python files and program the movements of the robot using python

Step5:

<br/>Execute the python program and record the movements.

## Program
```python
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis

    ## Write your code here
    from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis

    '''
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5]
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second) [0.5,2]
    '''

    ep_camera = ep_robot.camera

    ep_led = ep_robot.led

    print("Camera streaming started...")
    ep_camera.start_video_stream(display=True, resolution=camera.STREAM_360P)  

    ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on")   
    time.sleep(2)

    ep_chassis.move(x=2, y=0, z=0, xy_speed=0.75).wait_for_completed()

    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on")
    time.sleep(2)

    ep_chassis.drive_speed(x=0.3,y=0,z=25)
    time.sleep(15)
    ep_chassis.drive_speed(x=0,y=0,z=0)
    
        
    ep_led.set_led(comp="all",r=0,g=0,b=255,effect="on")
    time.sleep(2)        
    
 
    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=0.75).wait_for_completed()


    ep_camera.stop_video_stream()
    print("Stopped video streaming...")
    
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
https://youtube.com/shorts/t8nVyGZvT7w
Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

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
