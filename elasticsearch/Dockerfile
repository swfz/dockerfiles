FROM centos:centos6
MAINTAINER swfz <sawafuji.09@gmail.com>


COPY elasticsearch.repo /etc/yum.repos.d/elasticsearch.repo

RUN cat /etc/yum.repos.d/elasticsearch.repo
RUN yum -y install java-1.8.0-openjdk-devel.x86_64 nss elasticsearch

RUN /usr/share/elasticsearch/bin/plugin install analysis-kuromoji \
                                                royrusso/elasticsearch-HQ \
                                                polyfractal/elasticsearch-inquisitor


#VOLUME ["/data", "/logs"]

EXPOSE 9200 9300

CMD [""]

