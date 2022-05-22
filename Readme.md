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



