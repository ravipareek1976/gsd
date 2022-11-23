# Getting Started with Docker

Official repo for Getting Started with Docker video training course by [@nigelpoulton](https://twitter.com/nigelpoulton)

## first-container

This folder contains the files to build a single-container web app (express, handlebars...)
- Docker hub image: [nigelpoulton/gsd:first-ctr](https://hub.docker.com/repository/docker/nigelpoulton/gsd)

## multi-container

NEEDS UPDATING
This folder contains the files to build a multi-container web app with Compose.
- Pthon flask app with redis cache
- Docker hub image: [nigelpoulton/gsd:compose-app](https://hub.docker.com/repository/docker/nigelpoulton/gsd)

## swarm-stack

This folder contains the files to build a multi-container web app with Swarm Stacks.
- Pthon flask app with redis cache that also returns hostname of container servicing request
- Docker hub image: [nigelpoulton/gsd:swarm-stack](https://hub.docker.com/repository/docker/nigelpoulton/gsd)

## command executed on Dokcer website, could not clone git repo fro Docker Desktop
docker image build  -t 9871889667/gsd:first-ctr .
docker image ls
docker login   // 9871889667/docker@123@#$%
dockcer image push 9871889667/gsd:first-ctr        // it will push in https://hub.docker.com/repositories
docker image rm 9871889667/gsd:first-ctr       // delete loca copy to verrfy image at DokcerHUb repo
docker container run -d --name webravi -p 8000:8080 9871889667/gsd:first-ctr    // if image not avaialble loca pull from dokcer repo
dokcer container ls      // now check if doloaded image is running or not witht his command
then at web envrionment  : click open port 8000...it will launch the application succefully

dokcer container start webravi     // for starting and stoppin command
docker container stop webravi
