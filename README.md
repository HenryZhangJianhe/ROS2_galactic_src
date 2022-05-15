# 1 建包 
cpp
ros2 pkg create --build-type ament_cmake --node-name my_node my_package
python
ros2 pkg create --build-type ament_python --node-name my_node my_package

# 2 构建 
先对src的依赖下载
rosdep install -i --from-path src --rosdistro galactic -y
单独构建
colcon build --packages-select my_package
# 2 