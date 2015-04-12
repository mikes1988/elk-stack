FROM mikes1988/ubuntu-java8
MAINTAINER Michael Edwards <mikes1988@gmail.com>

RUN wget -O - http://packages.elasticsearch.org/GPG-KEY-elasticsearch |apt-key add -

RUN echo 'deb http://packages.elasticsearch.org/elasticsearch/1.4/debian stable main' |\
    tee /etc/apt/sources.list.d/elasticsearch.list

RUN DEBIAN_FRONTEND=noninteractive apt-get update

RUN DEBIAN_FRONTEND=noninteractive apt-get -y install elasticsearch

EXPOSE 9200

ENTRYPOINT /usr/share/elasticsearch/bin/elasticsearch
