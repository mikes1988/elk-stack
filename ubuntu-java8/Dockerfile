FROM ubuntu:latest

MAINTAINER Michael Edwards <mikes1988@gmail.com>

RUN export DEBIAN_FRONTEND=noninteractive && \
    apt-get update && \
    apt-get install -y software-properties-common && \
    add-apt-repository -y ppa:webupd8team/java && \
    apt-get update

RUN echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | \
    /usr/bin/debconf-set-selections && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y oracle-java8-installer