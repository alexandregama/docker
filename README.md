# Docker Container

### Containerization x Virtualization 

![](http://www.eweek.com/imagesvr_ce/8781/DockerFacts_3.jpg)

### Containerization technologies

- **LXC** (Linux Containers)
  This is the father of all kinds of containers and it represents an operating-system-level virtualization environment for running multiple isolated Linux system on a single Linux machine

- **OpenVZ**
  This is OS-level virtualization technology based on the Linux Kernel

- **The FreeBSD jail**
  This is a mechanism that implement and OS-level virtualization, which lets the administrations partition a FreeBSD-based computer system into several idependent mini-system called *jais*

### Undestanding the Docker setup

```bash
$ docker version
```

```bash
Client:
 Version:      1.8.2
 API version:  1.20
 Go version:   go1.4.2
 Git commit:   0a8c2e3
 Built:        Thu Sep 10 19:10:10 UTC 2015
 OS/Arch:      darwin/amd64

Server:
 Version:      1.8.2
 API version:  1.20
 Go version:   go1.4.2
 Git commit:   0a8c2e3
 Built:        Thu Sep 10 19:10:10 UTC 2015
 OS/Arch:      linux/amd64
```

```bash
$ docker info
```

```bash
Containers: 5
Images: 301
Storage Driver: aufs
 Root Dir: /mnt/sda1/var/lib/docker/aufs
 Backing Filesystem: extfs
 Dirs: 311
 Dirperm1 Supported: true
Execution Driver: native-0.2
Logging Driver: json-file
Kernel Version: 4.0.9-boot2docker
Operating System: Boot2Docker 1.8.2 (TCL 6.4); master : aba6192 - Thu Sep 10 20:58:17 UTC 2015
CPUs: 1
Total Memory: 1.956 GiB
Name: default
ID: WJHO:IK2U:XVXF:NIHY:VBP3:4CIP:H6TH:QGAR:7YQ7:C3EL:PVQD:CMIA
Debug mode (server): true
File Descriptors: 11
Goroutines: 16
System Time: 2015-12-26T11:47:45.40090594Z
EventsListeners: 0
Init SHA1:
Init Path: /usr/local/bin/docker
Docker Root Dir: /mnt/sda1/var/lib/docker
Username: alexandregama
Registry: https://index.docker.io/v1/
Labels:
 provider=virtualbox
```

### Downloading the first Docker image

- We will download images from Docker Registry

```bash
$ sudo docker pull busybox

511136ea3c5a: Pull complete
df7546f9f060: Pull complete
ea13149945cb: Pull complete
4986bf8c1536: Pull complete

busybox:latest: The image you are pulling has been verified. Important: image verification is a tech preview feature and should not be relied on to provide security.
Status: Downloaded newer image for busybox:latest
```

We can see all images that have been downloaded with the following command:

```bash
$ sudo docker images

REPOSITORY    TAG     IMAGE ID         CREATED      VIRTUAL SIZE
busybox       latest  4986bf8c1536     12 weeks ago 2.433 MB
```

We can search an specific image using **grep** command

```bash
$ sudo docker pull | grep busybox

busybox                          latest              fc0db02f3072        2 weeks ago         1.113 MB
```





