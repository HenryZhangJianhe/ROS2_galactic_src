# 本仓库是根据ROS2教程一步一步学习建立的
[https://docs.ros.org/en/galactic/](https://docs.ros.org/en/galactic/)
# 1 建包 
cpp
ros2 pkg create --build-type ament_cmake --node-name my_node my_package
python
ros2 pkg create --build-type ament_python --node-name my_node my_package

# 2 构建 
注意cmakelist和package.xml的依赖添加

先对src的依赖下载
rosdep install -i --from-path src --rosdistro galactic -y
单独构建
colcon build --packages-select my_package

# 3多机