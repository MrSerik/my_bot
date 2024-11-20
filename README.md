## Robot Package Template Serik

open gazebo with my map :
ros2 launch my_bot launch_sim.launch.py world:=./src/my_bot/worlds/serik.world

ros2 launch my_bot launch_robot.launch.py

teleop:
ros2 run teleop_twist_keyboard teleop_twist_keyboard

SLAM/map in rviz:
sudo apt install ros-foxy-rplidar-ros

ros2 launch slam_toolbox online_async_launch.py params_file:=./src/my_bot/config/mapper_params_online_async.yaml use_sim_time:=true

do not forget to open rviz2!

nav2:
ros2 launch nav2_bringup navigation_launch.py use_sim_time:=true



to install nav2:
sudo apt install ros-foxy-navigation2 ros-foxy-nav2-bringup

to instal mux(it help to control with different cmd_bel):
sudo apt install ros-foxy-twist-mux


colcon error:
source /opt/ros/foxy/setup.bash
sudo apt update
sudo apt install ros-foxy-ament-cmake

some times you need to delete all logs : rm -rf ~/.ros/log

