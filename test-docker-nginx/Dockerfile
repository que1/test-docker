# Version: 0.0.1
FROM centos
MAINTAINER que1 "que1@sina.com"
ENV REFRESHED_AT 2018-08-14
RUN yum -y update
RUN rpm -Uvh http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm
RUN yum install -y nginx
RUN mkdir -p /var/www/html
RUN groupadd -f www-data
RUN useradd -g www-data www-data
ADD nginx/global.conf /etc/nginx/conf.d/
ADD nginx/nginx.conf /etc/nginx/nginx.conf
EXPOSE 80

