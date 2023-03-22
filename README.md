这是 fast_lio2 的源码程序，目前只测试了用 velodyne 16进行建图的方法，另外目前该算法适配的是实车。
## 硬件环境
ubuntu 20.04 
ROS noetic
## 使用方法
1. git clone下来
2. 输入如下命令编译工程：
```shell
cd ws_livox
catkin_make
# 编译通过即可，目前测试可以直接编译通过，没有其他的问题
```
3. 运行方法
```shell
source ./devel/setup.bash
roslaunch fast_lio mapping_velodyne.launch
# 注意这样运行后，桌面不会出现 rviz ，如果想看到rviz ，请在mapping_velodyne.launch中将<arg name="rviz" default="false" />改为<arg name="rviz" default="true" />
```