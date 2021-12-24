# A docker image for Pi.Alert
All credit for Pi.Alert goes to:
[pucherot/Pi.Alert](https://github.com/pucherot/Pi.Alert).

The Docker image is available at [jokobsk/Pi.Alert - Docker
Hub](https://hub.docker.com/repository/docker/jokobsk/pi.alert).

## Changing configuration
Map the container folder `/home/pi/pialert/config` to your own folder containing `pialert.conf` and `version.conf`. I'd start by copying the default files from [here](https://github.com/pucherot/Pi.Alert/tree/main/config).

# Disclaimer
This is my second container and I might have used unconventional hacks so if anyone is more experienced, feel free to fork/create pull requests.
