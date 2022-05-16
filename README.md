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

# 3service
ros2 pkg create --build-type ament_cmake cpp_srvcli --dependencies rclcpp example_interfaces

ros2 pkg create --build-type ament_cmake cpp_pubsub_for_tuto_infa --dependencies rclcpp tutorial_interfaces
ros2 pkg create --build-type ament_cmake cpp_srvcli_for_tuto_infa --dependencies rclcpp tutorial_interfaces

# 4自定义接口 tutorial_interfaces

# 5more_interfaces
```python
ros2 pkg create --build-type ament_cmake more_interfaces
mkdir more_interfaces/msg


bool FEMALE=true
bool MALE=false

string first_name
string last_name
bool gender
uint8 age
string address


<buildtool_depend>rosidl_default_generators</buildtool_depend>

<exec_depend>rosidl_default_runtime</exec_depend>

<member_of_group>rosidl_interface_packages</member_of_group>


find_package(rosidl_default_generators REQUIRED)

```


