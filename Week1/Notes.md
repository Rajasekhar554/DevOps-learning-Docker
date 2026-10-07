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

DOCKER COMMANDS
===============

sudo systemctl docker status                          -- to check docker service is running or not
docker images                                         -- To see the docker images on docker host
ps -ef | grep -i "dockerd"                            -- To check the docker process
docker run -d -p 80:80 --name nginxcon nginx          -- To run nginx as a container - first it check whether the image is available locally or not if not it will                                                              download from docker hub and eun it as a container
docker ps                                             -- To see the running containers
docker exec -it nginxcon /bin/bash                    -- To go inside running container
docker logs 369b197ee9ce                              -- To see logs of a ruuning container
docker inspect 369b197ee9ce                           -- To see the details of a container
docker rm nginxcon                                    -- To remove stopped container
docker stop nginxcon                                  -- To stop the running container
docker ps -a                                          -- To check all containers including stopped containers
docker rmi f9ea18bfa4fa                               -- To delete an image
docker rm -f 369b197ee9ce                             -- To delete running container forcefully
docker run -d -p 80:80 --name tomcatcon tomcat:latest -- To start tomcat as a container
docker logs tomcatcon




