# Jenkins docker-compose

A project to setup Jenkins using docker-compose.
The goal of this project is to learn how to setup Jenkins to run on containers.

[![Build Status](https://travis-ci.org/BernardoSilva/jenkins-docker-compose.svg?branch=master)](https://travis-ci.org/BernardoSilva/jenkins-docker-compose)


## How to run

```sh
docker-compose build
docker-compose up
```


## How it works

There are 3 containers at the moment.

### jenkins-master

This container is responsible to run the actual Jenkins server.

### jenkins-data

This container is just running as a volume to be easier to map a volume into the `jenkins-master` container.
This way we can map a container volume to another container instead of trying to map the host directory into a container.

### nginx

This container is acting as a proxy to serve Jenkins on port 80 for now.


