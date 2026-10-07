Docker :

Docker is a containerisation platform that allows developers to pack their code,dendencies and libraries into a standard single unit called container. Container will run across multiple environments without any compatability issues.Containers are light weight , portable in nature.

Beofre docker some memory wastage will happen , applications will run on dev env , QA when we run the same application in prod it won't run properly due to compatability issues.

After docker memory sharing will happen and application will run consistently across any platform.

Docker is a cross platform and open source application.


Docker Architecture :: 

https://docs.docker.com/get-started/docker-overview/

Docker Installation on ubuntu :: 

sudo apt update -y
sudo apt install docker.io -y

docker -v

ps -ef | grep -i "dockerd"
sudo systemctl satus docker

sudo usermod -aG docker ubuntu

docker ps

Docker flow :: 

DF -->DI --> DC

Once if we write docker file we need to execute docker build command then docker image will create then if we run docker run command then docker container will create once docker container is created then we can start the conatiner and then we can stop the container.

