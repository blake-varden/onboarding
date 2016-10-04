# onboarding
Onboarding Document


## ROS

http://wiki.ros.org/indigo/Installation/Ubuntu

http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment


### Install ROS

```bash
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net --recv-key 0xB01FA116

sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116

sudo apt-get update

sudo apt-get install ros-indigo-desktop-full

sudo rosdep init

rosdep update

echo "source /opt/ros/indigo/setup.bash" >> ~/.bashrc

source ~/.bashrc

sudo apt-get install python-rosinstall
```
### Setup Environment

```bash

export ROS_ENV_DIR=~/ROSEnvs

mkdir -p ${ROS_ENV_DIR}/catkin_ws/src

pushd  ${ROS_ENV_DIR}/catkin_ws/src

catkin_init_workspace

pip install catkin_pkg

pushd ${ROS_ENV_DIR}/catkin_ws

catkin_make

popd

echo 'source ${ROS_ENV_DIR}/catkin_ws/devel/setup.bash' >> ~/.bashrc
```




