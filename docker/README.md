# Docker

## How to restart all the dockers containers

```bash
docker restart $(docker ps -q)
```

## How to use docker command without be root

1. Add the group `docker` if it's necesary.

```bash
sudo groupadd docker
```

2. Add your user to the docker group:

```bash
sudo usermod -aG docker $USER
```

3. Logout and login again to see the changes.

## How to see containers running by name and image

```bash
docker ps --format "{{.Names}} {{.Image}}"
```

## See container stats consumption

```bash
docker stats
```

## Clean machine about old and unused containers, images, networks 

**(Caution: It can remove useful resources)**

```bash
docker system prune
```

[More info](https://docs.docker.com/engine/reference/commandline/system_prune/)

## Copy files from/to container

```bash
docker cp <container id>:<container directory> <file>
docker cp <file> <container id>:<container directory>
```

## Export / import docker image 

```bash
docker save -o <path for generated tar file> <image name>
docker load -i <path to image tar file>
```

## Connect to runnning container (sh)

```bash
docker exec -it <container name> sh
```

## List all the names of containers 

```bash
docker container ls -a --format="{{ json .Names }}"
```

## Retag or add a new tag to one image

```bash
docker tag <source tag or hash> <new tag>
```

## How to list all the disk consumption 

```bash
docker system df
find /var/lib/docker/ -name "*.log" -exec ls -sh {} \; | sort -n -r | head -20
du -aSh /var/lib/docker/ | sort -n -r | head -n 10
```

## How to see docker container process

```bash
docker top <container hash>
```

## How to see docker service events

```bash
docker events
```

## How to updated files of docker after creation

```bash
docker diff <container hash>
```

## How to see all the steps of a Docker image creation

```bash
docker history <image hash>
```



***

- [Home](/README.md)
- [Docker](/docker/README.md)
- [Git](/git/README.md)
- [Kubernetes](/k8s/README.md)