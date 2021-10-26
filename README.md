## **Install Docker Engine**

#This script was developed on Debian Linux 10"
#Check version of Linux:"
```
head -1 /etc/os-release
```
#Move to current user home directory, where installation files will be hosted
#Update OS packages and install prerequisite packages
```
cd ~
sudo apt-get update && sudo apt-get upgrade && sudo apt-get install -y git curl
```
#Download and install Docker
```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
rm get-docker.sh
```
#The following version of Docker has been installed:"
```
docker --version
```
## **Install Docker compose**
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```
#Add the current user to the docker group
```
## **Add docker usergroud**
sudo groupadd docker
sudo usermod -aG docker `whoami`
```
>>You must reboot before running the setup script.
## **Clone git repository**
```
git clone https://github.com/truongcaoxuan/devOps.git
```

## **Deploy with docker-compose**
```
docker-compose up -d
```
**Stop the containers**
```
docker-compose stop
```
**Start the containers**
```
docker-compose start
```
**Stop and remove the containers**
```
docker-compose down
```
**Stop and remove the containers. Use -v to remove the volumes if looking to erase all data.**
```
docker-compose down -v
```



