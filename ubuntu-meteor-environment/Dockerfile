# Pull base image.
FROM docker.cn/docker/ubuntu:14.04

# Install deps
RUN cp /etc/apt/sources.list /etc/apt/sources.list.bak && \

    echo > /etc/apt/sources.list && \

    printf "\
deb http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse\n\
deb http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse\n\
deb http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse\n\
deb http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse\n\
deb http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse\n\
deb-src http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse\n\
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse\n\
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse\n\
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse\n\
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse" \
>> /etc/apt/sources.list && \

   # From http://docs.mongodb.org/manual/tutorial/install-mongodb-on-ubuntu/
   apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10 && \

   echo 'deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen' | sudo tee /etc/apt/sources.list.d/mongodb.list && \

   apt-get update && \

   # From https://github.com/joyent/node/wiki/installing-node.js-via-package-manager
   curl -sL https://deb.nodesource.com/setup | sudo bash - && \

   # Python is for node-gyp
   apt-get install -y vim screen curl git mongodb-org build-essential nodejs python && \

   npm install -g pm2 meteorite && \

   # From https://github.com/meteor/meteor
   curl https://install.meteor.com | /bin/sh

EXPOSE 3000 4000 5000 9000  27017 28017
