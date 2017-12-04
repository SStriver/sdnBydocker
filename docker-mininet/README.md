# docker-mininet #

The Docker image for [Mininet](http://mininet.org/)
## docker pull command ##

Download for [Docker Hub](https://hub.docker.com/)

    & docker pull sstriver/mininet

## docker run command ##

    & docker run -it --rm --privileged sstriver/mininet

## docker run with miniedit command ##

    $ docker run -it --rm --privileged -e DISPLAY \
     			-v /tmp/.X11-unix:/tmp/.X11-unix \
     			-v /lib/modules:/lib/modules \
     			sstriver/mininet