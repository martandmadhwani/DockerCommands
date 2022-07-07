# Introduction to Docker
Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers. 
The service has both free and premium tiers. 
The software that hosts the containers is called Docker Engine.
It was first started in 2013 and is developed by Docker, Inc

# Docker Basic Commands
- "" docker run <imagename>""
	-run the docker image if not available locally it will download image from dockerhub and run it.
	ex. docker run nginx

- "" docker run -it centos bash""
	- Run centos and show bash promt

- "" docker ps ""
	- list down running docker image with container id,imagename,command,createdOn,Status,Ports,and containername

- "" docker ps -a ""
	-list down running as well as priviously stopped containers.

- "" docker stop <containername> ""
     -stop container using containername

- "" docker rm <containername> ""
	-remove or delete container permenantly

- "" docker images ""
	-shows list of images available with local docker with sizes

- "" docker rmi <imagename> ""
	-Will remove unused image ** Delete all dependent containers to remove image **

- "" docker pull <imagename> ""
	-Will just pull image to local docker.

- "" docker exec <containername> cat /etc/hosts""
	-run command inside docker container to get the hosts.

- "" docker run **-d** kodekloud/simple-webapp ""
	-run docker container in background mode

- "" docker attache <containerid> ""
	- use docker attach to attach your terminal's standard input, output, and error (or any combination of the three) to a running container using the container's ID or name.
	 This allows you to view its ongoing output or to control it interactively, as though the commands were running directly in your terminal.

- "" docker run redis:4.0 ""
   - 4.0 is called tag
   - degault tag is latest

- "" docker run -p 80:5000 repo/webapp ""
	-p is used to map port 80 to internal docker port 5000

- "" docker run -v /opt/datadir:/var/lib/mysql mysql ""
	- mount external directory to docker of mysql to store mysql data

- "" docker inspect <containername>""
	- It will provide all details about container

- "" docker logs <cotainername>""
	- It will show logs of container which are running on -d mode or say in background

# Docker CLI
	- Docker CLI can be on diffrent client machine we can still run command by specifing host from clinet system to docker host.
	- for example, docker -H=remote-docker-engine:2375
				   docker -H=10.123.1.1:2375 run nginx



