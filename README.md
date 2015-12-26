# Docker
Docker commands

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
``

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

### Docker commands

#####docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]#####

#The Dockerfile build instructions#

## The FROM instruction ##

#####FROM \<image\>[:\<tag\>]#####

\<image\>: This is the name of the image which will be used as the base image
<tag>: This is the optional tag qualifier for that image. The tag latest is assumed when any tag has not been specified

Example

```go
FROM centos
```

```go
FROM ubuntu:14.04
```

## The MAINTAINER instruction ##

##### MAINTAINER \<author's details\>#####

## The Copy instruction ##

##### COPY <src> ... <dst> #####

\<src\> - This is the directory source
... - multiples source files can be specified
\<dst\> - This is the destination directory. It must be end with a slash



