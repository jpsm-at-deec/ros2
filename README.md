# ros2
notes on getting ros2[1]

[1] https://docs.ros.org/en/rolling/Installation/Alternatives/Ubuntu-Development-Setup.html

(jpsm@deec.uc.pt)

...

```
mkdir -p ~/ros2_rolling/src
cd ~/ros2_rolling
vcs import --input https://raw.githubusercontent.com/ros2/ros2/rolling/ros2.repos src
```

```
sudo apt upgrade
```

```
sudo rosdep init
rosdep update
rosdep install --from-paths src --ignore-src -y --skip-keys "fastcdr rti-connext-dds-6.0.1 urdfdom_headers"
```

```
cd ~/ros2_rolling/
colcon build --symlink-install
```
