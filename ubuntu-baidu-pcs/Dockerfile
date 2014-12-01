# Pull base image.
FROM docker.cn/docker/ubuntu

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

   apt-get update && \

   apt-get install -y make git libcurl4-openssl-dev && \

   git clone https://github.com/GangZhuo/baidupcs.git && \

   cd baidupcs && make clean && make && make install

