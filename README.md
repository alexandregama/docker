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



