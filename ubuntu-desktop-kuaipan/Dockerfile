# Pull base image.
FROM dockerfile/ubuntu-desktop

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

   apt-get install -y libqxt-gui0 libboost-iostreams1.54.0 && \

   wget https://launchpad.net/kuaipan4uk/2.0/2.0-beta/+download/kuaipan4uk_1404_2.0.0.3_amd64.deb && \

   dpkg -i kuaipan4uk_1404_2.0.0.3_amd64.deb
