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

**The VM is a hardware abstraction**: it takes physical CPUs and RAM from a host, and divides and shares it across several smaller virtual machines. There is an OS and application running inside the VM, but the virtualization software usually has no real knowledge of that.

**A container is an application abstraction**: the focus is really on the OS and the application, and not so much the hardware abstraction. Many customers actually use both VMs and containers today in their environments and, in fact, may run containers inside of VMs.

*Imagine booting up a virtual machine (VM), running a command and then killing it; it would take a minute or two just to boot the VM before running the command. A VM has to emulate a full hardware stack, boot an operating system, and then launch your app - it’s a virtualized hardware environment. Docker containers function at the application layer so they skip most of the steps VMs require and just run what is required for the app. Now you know why they say containers are fast!*

![DockerRun](https://training.play-with-docker.com/images/ops-basics-run-details.svg)
![DockerRunInstances](https://training.play-with-docker.com/images/ops-basics-instances.svg)
![DockerContainerInIsolation](https://training.play-with-docker.com/images/ops-basics-exec.svg)

Docker build

Creates a docker image using docker file

docker ps: lists the running containers [-a] => all

**Images**: The file system and configuration of our application which are used to create containers. To find out more about a Docker image, run docker image inspect alpine. In the demo above, you used the docker image pull command to download the alpine image. When you executed the command docker container run hello-world, it also did a docker image pull behind the scenes to download the hello-world image.


**Containers**: Running instances of Docker images — containers run the actual applications. A container includes an application and all of its dependencies. It shares the kernel with other containers, and runs as an isolated process in user space on the host OS. You created a container using docker run which you did using the alpine image that you downloaded. A list of running containers can be seen using the docker container ls command.


**Docker daemon**: The background service running on the host that manages building, running and distributing Docker containers.
Docker client - The command line tool that allows the user to interact with the Docker daemon.


**Docker Hub**: Store is, among other things, a registry of Docker images. You can think of the registry as a directory of all available Docker images. You’ll be using this later in this tutorial.

```console
docker container run -ti ubuntu bash
apt-get update
apt-get install -y figlet
figlet "hello docker"
exit
docker container ls -a
docker container commit CONTAINER_ID
docker image ls
docker image tag <IMAGE_ID> ourfiglet
docker image ls
```

[further readings](https://training.play-with-docker.com/ops-s1-images/)
