## Requirement

- Docker Engine (\>= 19.03)
- NVIDIA Driver
- [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html#docker)

## How to run

- http://wiki.ros.org/docker/Tutorials

### Without GUI

```shell
$ docker run -it --rm osrf/ros:melodic-desktop-full /bin/bash
$ source ros_entrypoint.sh
```



### Basic GUI

```shell
$ docker run -it\
    --rm \
    -e DISPLAY \
    -v /etc/localtime:/etc/localtime:ro \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    osrf/ros:melodic-desktop-full \
    /bin/bash
```

> Only simple rqt visualization tools other than Rviz and Gazebo can be used.



### Hardware Acceleration

- http://wiki.ros.org/action/login/docker/Tutorials/Hardware%20Acceleration#nvidia-docker2


```shell
$ docker build -t ros-opengl .
$ xhost +
$ ./run.sh
```

