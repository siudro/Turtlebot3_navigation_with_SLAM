# Turtlebot3_navigation_with_SLAM
SLAM (Simultaneous Localization and Mapping) is one of the most useful nodes in ROS, where it uses the robot's sensors to explore and draw a map of the surroundings. We can use SLAM approach with a variety of robots. In this repo, I tried to virtually navigate turtlebot3 in the map I saved [before](https://github.com/siudro/Building-SLAM-map-with-TURTLEBOT3/blob/main/map.png).

first I needed to launch Gazebo:
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
then running the navigation node:
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```


the map I saved before will show up, now I have to make the lidar sensors data match with the map by clicking on 2D pose estimate and moving the robot.
![turtlebot3_navigation](https://user-images.githubusercontent.com/83130573/128492787-ca370293-82ab-482c-9f52-c03fac8a666f.PNG)


now to move the bot with keyboard:
```
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

![teleop turtlebot3 navigation](https://user-images.githubusercontent.com/83130573/128492855-371df273-67fc-4001-ba0f-bce15ef03fa6.PNG)
