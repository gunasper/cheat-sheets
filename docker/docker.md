# Docker
Docker is a computer program that performs operating-system-level virtualization, also known as "containerization". This document is my cheat sheet to common operations that I always forget how to perform.

## docker ps 
Lists running containers. Some useful flags include: -a / -all for all containers (default shows just running) and —-quiet /-q to list just their ids (useful for when you want to get all the containers).

## docker build
The docker build command builds Docker images from a Dockerfile and a “context”. A build’s context is the set of files located in the specified PATH or URL. Use the -t flag to label the image, for example docker build -t my_container . with the . at the end signalling to build using the currently directory.

## docker logs
Use this command to display the logs of a container, you must specify a container and can use flags, such as --follow to follow the output in the logs of using the program. docker logs --follow my_container

## delete all stopped containers
docker rm $(docker ps -a -q)

## kill all running containers
docker kill $(docker ps -q)

# delete all images
docker rmi $(docker images -q)
