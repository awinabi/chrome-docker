## Chrome on Docker

Run older versions of chrome in docker and connect to it with VNC

- Courtesy: https://medium.com/dot-debug/running-chrome-in-a-docker-container-a55e7f4da4a8


### Steps

- Download the required chrome version from slimjet -https://www.slimjet.com/chrome/google-chrome-old-version.php
- Edit Docker file as required
- Build image
```
sudo docker build -t chrome:60 .
```
- Run image
```
sudo docker run -p 5900:5900 -e VNC_SERVER_PASSWORD=password --user apps --privileged chrome:60
```

- View using a VNC viewer. for eg. `krdc` in ubuntu
```
sudo apt-get install krdc
```



