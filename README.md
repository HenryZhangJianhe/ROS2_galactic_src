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

# 3���

# 4���밲װros2 
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
