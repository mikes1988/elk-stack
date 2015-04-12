FROM ubuntu-java8

MAINTAINER Michael Edwards <mikes1988@gmail.com>

RUN wget -O - http://packages.elasticsearch.org/GPG-KEY-elasticsearch |apt-key add -

RUN echo 'deb http://packages.elasticsearch.org/logstash/1.5/debian stable main' |tee /etc/apt/sources.list.d/logstash.list

RUN export DEBIAN_FRONTEND=noninteractive &&\
    apt-get update &&\
    apt-get install -y logstash
    
EXPOSE 5000

ENTRYPOINT /opt/logstash/bin/logstash agent -f /etc/logstash/conf.d/