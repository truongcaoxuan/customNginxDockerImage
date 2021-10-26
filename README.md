**Install Docker compose**
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```
**Deploy with docker-compose**
```
$ docker-compose up -d
```
**Stop the containers**
```
$ docker-compose stop
```
**Start the containers**
```
$ docker-compose start
```
**Stop and remove the containers**
```
$ docker-compose down
```
**Stop and remove the containers. Use -v to remove the volumes if looking to erase all data.**
```
$ docker-compose down -v
```



