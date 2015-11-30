# Docker
Docker commands

#The Docker run#

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



