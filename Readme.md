//Docker for Linux ubuntu 22

//Insatllation

sudo apt -y update

sudo apt -y install apt-transport-https ca-certificates curl gnupg-agent software-properties-common

sudo apt remove docker docker-engine docker.io containerd runc

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/docker-archive-keyring.gpg

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"


//Finally install Docker CE on Ubuntu22.04|20.04|18.04:
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io

//Add your user account to docker group.
sudo usermod -aG docker $USER
newgrp docker


//Images
docker images
docker run -ti ubuntu:latest bash   //ti means terminal interactive , run bash

docker ps image --format //check running images

docker ps -a //see container, -a see all containers, -l last contaiiner

docker commit containerid // to create image from container 

docker tag imageId imagename // chnage name

docker run -rm // -rm remove the container afterwards

docker run -d -ti ubuntu:latest bash // --detach or -d , means that a Docker container runs in the background of your terminal.

Detached mode, started by the option --detach or –d flag in docker run command, means that a Docker container runs in the background of your terminal. It does not receive input or display output. Using detached mode also allows you to close the opened terminal session without stopping the container. 

//Adding more things to running container
docker exce //The docker exec command runs a new command in a running container.










