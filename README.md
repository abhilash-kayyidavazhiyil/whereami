# SLAM map my world

.whereami/
├── CMakeLists.txt
├── README.md
├── ball_chaser
│   ├── CMakeLists.txt
│   ├── launch
│   │   └── ball_chaser.launch
│   ├── package.xml
│   ├── src
│   │   ├── drive_bot.cpp
│   │   └── process_image.cpp
│   └── srv
│       └── DriveToTarget.srv
├── images
│   ├── Screenshot\ from\ 2021-04-01\ 11-23-18.png
│   ├── Screenshot\ from\ 2021-04-01\ 11-27-45.png
│   ├── Screenshot\ from\ 2021-04-01\ 11-27-57.png
│   └── Screenshot\ from\ 2021-04-01\ 11-30-47.png
└── my_robot
    ├── CMakeLists.txt
    ├── config
    │   ├── base_local_planner_params.yaml
    │   ├── costmap_common_params.yaml
    │   ├── global_costmap_params.yaml
    │   └── local_costmap_params.yaml
    ├── launch
    │   ├── amcl.launch
    │   ├── localization.launch
    │   ├── mapping.launch
    │   ├── robot_description.launch
    │   └── world.launch
    ├── maps
    │   ├── map.pgm
    │   └── map.yaml
    ├── meshes
    │   └── hokuyo.dae
    ├── package.xml
    ├── rviz
    │   └── config_file.rviz
    ├── urdf
    │   ├── my_robot.gazebo
    │   └── my_robot.xacro
    └── worlds
        ├── ball.world
        ├── ball_house.world
        ├── build_my_world.world
        └── empty.world

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


