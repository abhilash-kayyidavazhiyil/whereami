# SLAM map my world

    .map_my_world# Map My World Project
    ├── my_robot     # my_robot package                   
    │   ├── launc                                        # launch folder for launch files   
    │   │   ├── robot_description.launch
    │   │   ├── world.launch
    │   ├── meshes                     # meshes folder for sensors
    │   │   ├── hokuyo.dae
    │   ├── urdf                       # urdf folder for xarco files
    │   │   ├── my_robot.gazebo
    │   │   ├── my_robot.xacro
    │   ├── world                      # world folder for world files
    │   │   ├── <yourworld>.world
    │   ├── CMakeLists.txt             # compiler instructions
    │   ├── package.xml                # package info
    ├── ball_chaser                    # ball_chaser package                   
    │   ├── launch                     # launch folder for launch files   
    │   │   ├── ball_chaser.launch
    │   ├── src                        # source folder for C++ scripts
    │   │   ├── drive_bot.cpp
    │   │   ├── process_images.cpp
    │   ├── srv                        # service folder for ROS services
    │   │   ├── DriveToTarget.srv
    │   ├── CMakeLists.txt             # compiler instructions
    │   ├── package.xml                # package info                  
    └──   

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


