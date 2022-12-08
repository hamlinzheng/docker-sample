## How to Run

1. Install basic dependency

   ```shell
   $ sudo apt install x11-xserver-utils
   ```

2. Provide X11 permission

   ```shell
   # Allow X server connection
   $ xhost +
   
   # Disallow X server connection
   $ xhost -
   ```

3. Build dockerfile and run

   ```shell
   $ docker build -t firefox .
   $ docker run \
       --rm \
       -e DISPLAY \
       -v /etc/localtime:/etc/localtime:ro \
       -v /tmp/.X11-unix:/tmp/.X11-unix \
       firefox
   ```

## TODO

- [ ] Encoder
- [ ] Zoom
