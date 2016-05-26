FROM centos:centos6
MAINTAINER swfz <sawafuji.09@gmail.com>

RUN yum install -y epel-release
RUN yum --enablerepo=epel install -y redis

RUN sed s/bind\ 127.0.0.1/bind\ 0.0.0.0/ -i /etc/redis.conf
RUN sed s/daemonize\ yes/daemonize\ no/ -i /etc/redis.conf
EXPOSE 6379

ENTRYPOINT ["service", "redis", "start" ]
