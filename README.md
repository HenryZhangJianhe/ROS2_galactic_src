# ���ֿ��Ǹ���ROS2�̳�һ��һ��ѧϰ������
[https://docs.ros.org/en/galactic/](https://docs.ros.org/en/galactic/)
# 1 ���� 
cpp
ros2 pkg create --build-type ament_cmake --node-name my_node my_package
python
ros2 pkg create --build-type ament_python --node-name my_node my_package

# 2 ���� 
ע��cmakelist��package.xml���������

�ȶ�src����������
rosdep install -i --from-path src --rosdistro galactic -y
��������
colcon build --packages-select my_package

# 3service
ros2 pkg create --build-type ament_cmake cpp_srvcli --dependencies rclcpp example_interfaces

ros2 pkg create --build-type ament_cmake cpp_pubsub_for_tuto_infa --dependencies rclcpp tutorial_interfaces
ros2 pkg create --build-type ament_cmake cpp_srvcli_for_tuto_infa --dependencies rclcpp tutorial_interfaces

