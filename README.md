# 1 ���� 
cpp
ros2 pkg create --build-type ament_cmake --node-name my_node my_package
python
ros2 pkg create --build-type ament_python --node-name my_node my_package

# 2 ���� 
�ȶ�src����������
rosdep install -i --from-path src --rosdistro galactic -y
��������
colcon build --packages-select my_package
# 2 