ELK Stack
=========

Purpose
-------
Just a basic ELK stack, with each element containerized.

Getting Started
---------------

### Building

Simply run `./build`, this does a few things:

* Pulls official ubuntu docker repository
  - Used for all future images
* Builds ubuntu-java8
  - This is used for elasticsearch and logstash images
* Finally builds and tags elasticsearch, kibana and logstash images.

### Pulling

If you trust me or can't be bothered building everything yourself you can just pull everything from docker hub:

* `docker pull mikes1988/ubuntu-elasticsearch`
* `docker pull mikes1988/ubuntu-kibana`
* `docker pull mikes1988/ubuntu-logstash`