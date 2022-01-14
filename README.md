# A docker image for Pi.Alert
All credit for Pi.Alert goes to:
[pucherot/Pi.Alert](https://github.com/pucherot/Pi.Alert).

The Docker image is available at [jokobsk/Pi.Alert - Docker
Hub](https://registry.hub.docker.com/r/jokobsk/pi.alert).

The source Docker file is available [here on GitHub](https://github.com/jokob-sk/Docker-Image-for-Pi.Alert).

## Changing the configuration

- Download `pialert.conf` and `version.conf` from [here](https://github.com/pucherot/Pi.Alert/tree/main/config).
- Map the container folder `/home/pi/pialert/config` to your own folder containing `pialert.conf` and `version.conf`. 
- In `pialert.config` specify your network adapter (will probably be eth0 or eth1) and the network filter, e.g. if your DHCP server assigns IPs in the 192.168.1.0 to 192.168.1.255 range specify it the following way: `SCAN_SUBNETS    = '192.168.1.0/24 --interface=eth0'`

### Database backup and restore

The docker image creates a DB copy once an hour copying the DB to `/home/pi/pialert/config/pialert.db_bak`

You can backup the DB by also ad-hoc by running the follow command in the container:

`cp /home/pi/pialert/db/pialert.db /home/pi/pialert/config/pialert.db_bak`

Restoring the DB:

`cp /home/pi/pialert/config/pialert.db_bak /home/pi/pialert/db/pialert.db`

## Running the container
You will have to probably run the container on the host network, e.g: `sudo docker run --rm --net=host jokobsk/pi.alert`

## Port 

The container runs on the port `:20211`.

## UI URL

The UI is located on `<host IP>:20211/pialert/`

Please note - the cronjob is executed every 1, 5 and 15 minutes so wait that long for all of the scans to run.

# Disclaimer
This is my second container and I might have used unconventional hacks so if anyone is more experienced, feel free to fork/create pull requests.


<a href="https://www.buymeacoffee.com/jokobsk" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 30px !important;width: 117px !important;" width="150px" ></a>
