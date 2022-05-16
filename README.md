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

# 4编译安装ros2 
ubunut18 ele 

--- stderr: foonathan_memory_vendor
Cloning into 'foo_mem-ext'...
Note: checking out 'v0.7-1'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b <new-branch-name>

HEAD is now at 19ab075 Release 0.7-1
