# A docker image for Pi.Alert
All credit for Pi.Alert goes to:
[pucherot/Pi.Alert](https://github.com/pucherot/Pi.Alert).

The Docker image is available at [jokobsk/Pi.Alert - Docker
Hub](https://registry.hub.docker.com/r/jokobsk/pi.alert).

The source Docker file is available [here on GitHub](https://github.com/jokob-sk/Docker-Image-for-Pi.Alert).

## Changing the configuration
Map the container folder `/home/pi/pialert/config` to your own folder containing `pialert.conf` and `version.conf`. I'd start by copying the default files from [here](https://github.com/pucherot/Pi.Alert/tree/main/config).


## Port mapping

Map port `:20211` on the container to your local port.

## UI URL

The UI is located on `<host IP>:<local port>/pialert/`

# Disclaimer
This is my second container and I might have used unconventional hacks so if anyone is more experienced, feel free to fork/create pull requests.
