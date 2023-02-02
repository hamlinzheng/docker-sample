

```
$ docker run -it \
    --rm \
    -e DISPLAY \
    -v /etc/localtime:/etc/localtime:ro \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    --network host \
    --privileged \
    --gpus all \
    nvidia/opengl:1.0-glvnd-runtime-ubuntu20.04 \
    /bin/bash

```
