# Task1-installations-Ros
Welcome to the Task1-installations-Ros wiki!

1 Setup your sources.list Setup your computer to accept software from packages.ros.org.

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

2 Set up your keys sudo apt install curl # if you haven't already installed curl

curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

3 Installation First, make sure your Debian package index is up-to-date:

sudo apt update

Desktop-Full Install: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages

sudo apt install ros-noetic-desktop-full

Desktop Install: Everything in ROS-Base plus tools sudo apt install ros-noetic-desktop

ROS-Base: (Bare Bones) ROS packaging, build, and communication libraries. No GUI tools.

sudo apt install ros-noetic-ros-base

sudo apt install ros-noetic-PACKAGE

sudo apt install ros-noetic-slam-gmapping

apt search ros-noetic

4 Environment setup You must source this script in every bash terminal you use ROS in.

source /opt/ros/noetic/setup.bash

Bash

echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc

source ~/.bashrc

Zsh

echo "source /opt/ros/noetic/setup.zsh" >> ~/.zshrc

source ~/.zshrc

5 Dependencies for building packages

To install this tool and other dependencies for building ROS packages, run:

sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential

Initialize rosdep

sudo apt install python3-rosdep

sudo rosdep init

rosdep update

and done * _ *

