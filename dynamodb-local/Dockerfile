FROM centos:centos6
MAINTAINER swfz <sawafuji.09@gmail.com>

RUN yum install -y curl-devel java-1.8.0-openjdk-devel.x86_64
RUN curl -LO http://dynamodb-local.s3-website-us-west-2.amazonaws.com/dynamodb_local_latest
RUN tar zxvf dynamodb_local_latest

EXPOSE 8000

RUN mkdir db
ENTRYPOINT ["java","-Djava.library.path=./DynamoDBLocal_lib","-jar","DynamoDBLocal.jar","-dbPath","./db"]

