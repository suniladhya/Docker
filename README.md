# Docker

## Components

![DockerComponent](https://docs.docker.com/engine/images/architecture.svg)

### Client

Where the commands are run

### Registry

Where the images reside

## Container

Containers are the running instances of the Docker Images.
A container image is a lightweight, stand-alone, executable package of a piece of software that includes everything needed to run it: code, runtime, system tools, system libraries, settings.

Features of Containers:

1. Are lightweight

2. Fewer resources are used

3. Booting of containers is very fast

4. Can start, stop, kill, remove containers easily and quickly

5. Operating System resources can be shared within Docker

6. Containers run on the same machine sharing the same Operating system Kernel, this makes it faster

7. You can use the command - docker container create
to create a container in stopped state

[What is a Container](https://www.docker.com/resources/what-container)

## Useful Links

[Docs](https://docs.docker.com/get-docker/)
| [1](https://www.docker.com/blog/best-way-learn-docker-free-play-docker-pwd/)
| [Play With Docker](https://training.play-with-docker.com/)
| [pwd Console](http://play-with-docker.com/)
| [Docker hub](https://hub.docker.com/)

## Commands

```console
docker help
docker image ls
docker run hello-world
docker build
docker ps
docker ps -a
docker run ImageName
docker start ContainerName/ID
docker stop ContainerName/I
docker pause ContainerName/ID
docker unpause  ContainerName/I
docker top ContainerName/ID
docker stats ContainerName/I
docker attach ContainerName/I
docker kill ContainerName/ID
docker rm ContainerName/I
docker history ImageName/ID
```

![Docker Basic](https://training.play-with-docker.com/images/ops-basics-hello-world.svg)

Docker run 

1. looks for the image from the image list avsilable locally. (searches default registry if not available locally and fetch a local copy)

2. Creates an insatance of the image and executes it

Docker build

Creates a docker image using docker file

docker ps: lists the running containers [-a] => all