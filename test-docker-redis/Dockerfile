FROM ubuntu
MAINTAINER que1 que1@sina.com
ENV REFRESHED_AT 2018-08-15

RUN apt-get update

RUN apt-get -y install redis-server redis-tools

EXPOSE 6379
ENTRYPOINT ["/usr/bin/redis-server"]
CMD []
