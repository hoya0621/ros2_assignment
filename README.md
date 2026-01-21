# ros2_assignment

### ros2 installation

moveit 설치
sudo apt install -y ros-humble-moveit

doosan robot 깃 다운로드
cd src
git clone https://github.com/DoosanRobotics/doosan-robot2.git -b humble

rosdep 설치
sudo apt install -y python3-rosdep

실행
sudo rosdep init
rosdep update 

doosan 
cd ~/ros2_ws
rosdep install --from-paths src --ignore-src -r -y

colcon 설치
sudo apt install -y python3-colcon-common-extensions


sudo apt install -y \
  python3-numpy \
  python3-empy \
  python3-yaml \
  python3-colcon-common-extensions \
  ros-humble-moveit \
  ros-humble-rviz2

colcon build
source /opt/ros/humble/setup.bash
source install/setup.bash


ros2 launch dsr_moveit_config_e0509 start.launch.py
