# smarthome
MQTT Telegraf Influx Grafana HomeAssistant

## To get up and running
```
sudo apt update
sudo apt install git docker docker-compose
git pull https://github.com/Setcover/smarthome.git
cd smarthome
```
You might need to replace "docker" with "docker.io". When? Whenever apt complains about not finding any docker.

Look through all the files including subdirectories, comment or uncomment configuration as needed, maybe change the default password in `docker-compose.yml` and `telegraf/telegraf.conf`.

**Everything should work on a raspberry pi and on a pc, except "heimdall" and "influxdb". For those containers two images are present in the docker-compose.yml you have to select the correct one. (the one containing "arm" is for Raspberry Pi)**

When reasonably confident, start everything using `sudo docker-compose up -d`. You can check the logs using `sudo docker logs containername`.

Other useful commands are
```
sudo docker-compose up
sudo docker-compose down
sudo docker-compose pull # to update
sudo docker-compose start containername
sudo docker-compose stop containername
sudo docker-compose restart containername
sudo docker-compose up -d --force-recreate (containername)
sudo docker stats (you won't get any memory stats on a raspberry pi, kill it with CTRL + C)
sudo docker system prune (to remove unused docker images. Careful, do not use after "sudo docker-compose down" because all your images will be unused at this point and every image you need has to be downloaded again)
```
