FROM ubuntu:latest

MAINTAINER Michael Edwards <mikes1988@gmail.com>

RUN export DEBIAN_FRONTEND=noninteractive && \
    apt-get update && \
    apt-get install -y curl

RUN mkdir -p /opt/kibana && \
cd /opt/kibana && \
curl -O https://download.elasticsearch.org/kibana/kibana/kibana-4.0.1-linux-x64.tar.gz && \
tar -xf kibana-4.0.1-linux-x64.tar.gz --wildcards --anchored --strip-components=1 kibana-4*/

EXPOSE 5601

ENTRYPOINT /opt/kibana/bin/kibana