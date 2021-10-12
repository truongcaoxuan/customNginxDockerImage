#Build Docker image
sudo docker build -t nginx:custom .

#Run docker container from image
sudo docker run -d -p 80:80 nginx:custom
# customNginxDockerImage
