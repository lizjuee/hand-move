# bionic arm
bionic arm control

<p align="center">
<img src="https://github.com/qq44642754a/mechanical-arm/blob/master/serial_test/media/run_service.png" width="400">
<img src="https://github.com/qq44642754a/mechanical-arm/blob/master/serial_test/media/service_call.png" width="400">

# serial_test
use rosservice  control bionic arm move

# develop environment：
Ubuntu 16.04 + ros kinetic &&  Ubuntu 18.04 + ros melodic

# sensor：

intel realsense d435

# hardware equipment：

Ti5hand bionic arm
  
#setup:
```
$mkdir your_ws
     
$cd your_ws/
     
$mkdir src && cd src/
     
$git clone https://github.com/qq44642754a/mechanical-arm.git
     
$cd ..
     
$catkin_make
```


# run bionic arm:

## 1.connect serial port to control unit:
```
$cd /dev && ls
```
#### ps： when saw ttyUSBx equipment，it means the bionic arm is connected
## 2.run "moveHand service" program:
```
$rosrun serial_test move_hand_service.py
```

## 3.call /move_hand service in terminal:
```
$rosservice call /move_hand "type: 1"
```

### service query type of the demo

|request| action|
|:----:| -------------|
|1 | Open|
|2 | Fist|
|3 | Index finger|
|4| Middle finger|
|5| Ring finger|
|6| Little finger|
|7| Ok|


