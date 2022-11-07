# smarthome
MQTT Telegraf Influx Grafana HomeAssistant

## To get up and running
```
sudo apt update
sudo apt install git docker docker-compose
git pull https://github.com/Setcover/smarthome.git
cd smarthome
```
Look through all the files including subdirectories, comment or uncomment configuration as needed, maybe change the default password in `docker-compose.yml` and `telegraf/telegraf.conf`.

When reasonably confident, start everything using `sudo docker-compose up -d`. You can check the logs using `sudo docker logs containername`.

Other useful commands are
```
sudo docker-compose up
sudo docker-compose down
sudo docker-compose pull # to update
sudo docker-compose start containername
sudo docker-compose stop containername
sudo docker-compose restart containername
sudo docker-compose up -d --force-recreate
```
