## docker-ubuntu-baidu-pcs

you can see [ubuntu-desktop](https://github.com/dockerfile/ubuntu-desktop/blob/master/README.md) too.

### Base Docker Image

* [docker.cn/docker/ubuntu](https://docker.cn/docker/ubuntu)


### Installation

1. Install [Docker](https://www.docker.com/).

2. 
  Pull docker-ubuntu-docker-for-kuaipan `docker pull scarletsky/ubuntu-baidu-pcs`

   (alternatively, you can build an image from Dockerfile: `docker build -t="scarletsky/ubuntu-baidu-pcs" github.com/scarletsky/ubuntu-baidu-pcs`)


### Usage

```bash
$ docker run -it scarletsky/ubuntu-baidu-pcs /bin/bash
# pcs --help
# you can do something with pcs
```

### sp thanks
[GangZhuo](https://github.com/GangZhuo) 's great project: [baidupcs](https://github.com/GangZhuo/baidupcs)


