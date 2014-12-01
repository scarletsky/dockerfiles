## docker-ubuntu-desktop-for-kuaipan

you can see [ubuntu-desktop](https://github.com/dockerfile/ubuntu-desktop/blob/master/README.md) too.

### Base Docker Image

* [dockerfile/ubuntu-desktop](http://dockerfile.github.io/#/ubuntu-desktop)


### Installation

1. Install [Docker](https://www.docker.com/).

2. 
  Pull docker-ubuntu-docker-for-kuaipan `docker pull scarletsky/ubuntu-desktop-for-kuaipan`

   (alternatively, you can build an image from Dockerfile: `docker build -t="scarletsky/ubuntu-desktop-for-kuaipan" github.com/scarletsky/docker-ubuntu-desktop-for-kuaipan`)


### Usage

    docker run -it --rm -p 5901:5901 -e USER=root scarletsky/ubuntu-desktop-for-kuaipan \
        bash -c "vncserver :1 -geometry 1280x800 -depth 24 && tail -F /root/.vnc/*.log"

Connect to `vnc://<host>:5901` via VNC client.

