FROM centos
MAINTAINER que1 que1@sina.com
ENV REFRESHED_AT 2018-08-15

RUN yum -y update



#RUN yum install -y ruby ruby-devel 
#RUN yum install centos-release-scl-rh
#RUN yum install -y rh-ruby23
#RUN scl enable rh-ruby23 bash
RUN yum groupinstall -y "Development Tools"
RUN yum install -y http://rpms.famillecollet.com/enterprise/remi-release-7.rpm

#RUN yum install -y cmake
#RUN yum install -y build-essential zlib1g-dev libyaml-dev libssl-dev libgdbm-dev libreadline-dev libncurses5-dev libffi-dev 
#RUN yum install -y curl git-core openssh-server redis-server postfix checkinstall libxml2-dev libxslt-dev libcurl4-open
#RUN yum install -y ssl-dev libicu-dev mysql-client libmysqlclient-dev libreadline6-dev
RUN cd /tmp && mkdir ruby && cd ruby && curl --progress http://cache.ruby-lang.org/pub/ruby/2.3/ruby-2.3.2.tar.gz | tar xz && cd ruby-2.3.2 && ./configure && make && sudo make install

RUN gem install --no-rdoc --no-ri sinatra json redis

RUN mkdir -p /opt/webapp

EXPOSE 4567

CMD ["/opt/webapp/bin/webapp"]
