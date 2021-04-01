# SLAM map my world

Directory structure:

<img width="436" alt="Screen Shot 2021-04-01 at 12 16 09 PM" src="https://user-images.githubusercontent.com/16000838/113264513-1a842a00-92e4-11eb-819d-a0a98d745a0d.png">


Build:
```
catkin_make

source devel/setup.bash

roslaunch my_robot world.launch
```

next terminal
```
source devel/setup.bash

roslaunch my_robot mapping.launch
```

next terminal
```
source devel/setup.bash

rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

## instructions
- move the robot in the environment to create the Map

View the created map

```
rtabmap-databaseViewer ~/.ros/rtabmap.db
```

## results

IMG-20210401-WA0032.jpg![image](https://user-images.githubusercontent.com/16000838/113263432-d2b0d300-92e2-11eb-9b52-36f7f013593d.png)
IMG-20210401-WA0033.jpg![image](https://user-images.githubusercontent.com/16000838/113263471-de9c9500-92e2-11eb-828e-eec4b5ca099e.png)
IMG-20210401-WA0031.jpg![image](https://user-images.githubusercontent.com/16000838/113263486-e3f9df80-92e2-11eb-8cb6-93fca22d0bcd.png)
IMG-20210401-WA0034.jpg![image](https://user-images.githubusercontent.com/16000838/113263491-e78d6680-92e2-11eb-8d7f-23dccb848d97.png)


