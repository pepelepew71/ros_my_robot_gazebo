# ros_my_robot_gazebo

A collection of robots I ever used.

For spawning multiple robots in gazebo, you can setup different ```group ns``` and ```arg ns``` in ```launch/main.launch```. As shown in following:

```xml
    <group ns="car1">
        <include file="$(find ros_my_robot_gazebo)/launch/leo_rover/spawn.launch">
            <arg name="ns" value="car1" />
            .
            .
            .
    <group ns="car2">
        <include file="$(find ros_my_robot_gazebo)/launch/leo_rover/spawn.launch">
            <arg name="ns" value="car2" />
```

And also notice that the spawn location shouldn't overlap to other robot.
