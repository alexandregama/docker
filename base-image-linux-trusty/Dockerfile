############################################################
# Dockerfile to build a images based on Ubuntu Trusty version
# Based on Ubuntu Trusty
############################################################

# Set the base image to ubuntu
FROM ubuntu:trusty

# File Author / Maintainer
MAINTAINER Alexandre Gama <alexandre.gama.lima@gmail.com>

# Update the sources list and install base packages
RUN apt-get update && apt-get install -y \
	tar \
	less \
	git \
	curl \
	vim \
	wget \
	unzip \
	netcat \
	software-properties-common \
	telnet && \
	wget -P /usr/local/bin https://github.com/outbrain/zookeepercli/releases/download/v1.0.10/zookeepercli && \
	chmod 755 /usr/local/bin/zookeepercli && \
	wget https://github.com/coreos/etcd/releases/download/v2.2.2/etcd-v2.2.2-linux-amd64.tar.gz -P /tmp/etcd && \
	tar -xvf /tmp/etcd/etcd-v2.2.2-linux-amd64.tar.gz -C /tmp/etcd && \
  mv /tmp/etcd/etcd-v2.2.2-linux-amd64/etcdctl /usr/local/bin && \
  rm -R /tmp/etcd
