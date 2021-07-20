standard-environment
===========
[![](https://img.shields.io/github/license/MUCAer/standard-environment)](https://github.com/MUCAer/standard-environment/blob/main/LICENSE)
[![](https://github.com/MUCAer/standard-environment/workflows/Docker-Image-CI/badge.svg)](https://github.com/MUCAer/standard-environment/actions)
[![Docker-Image-Publish](https://github.com/MUCAer/standard-environment/actions/workflows/docker-publish.yml/badge.svg)](https://github.com/MUCAer/standard-environment/actions/workflows/docker-publish.yml)

# How to use?
You can use the docker image `machineplay/gcc10-standard-env` on the dockerhub directly.  
Or you can just build you own image use the docker file by `docker build`:  
```
docker build -t your-image-name .
```   
It also support docker compose, use the docker-compose.yml directly:  
```
//start the environment
docker compose up -d 
//jail into the container 
docker exec -ti container_name /bin/bash
```

# What tools the docker file has?
- include a standard Ubuntu 20.04 system
- cmake
- build-essential
- bison 
- flex 
- vim 
- make 
- git 
- gcc-10 
- g++-10
- psmisc 
- libncurses5-dev 
- zlib1g-dev 
- python3 
- autoconf 
- automake 
- libtool 
- curl  
- unzip 
- cmake
- tarscpp

