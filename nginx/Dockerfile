# Dockerizing nginx: Dockerfile for building nginx images
# Based on ubuntu
FROM ubuntu

MAINTAINER Francisco Oliveira <delley.fx@gmail.com>

RUN apt-get update

RUN apt-get install -y nginx

ADD nginx-config /etc/nginx/sites-enabled/default

RUN echo "daemon off;" >> /etc/nginx/nginx.conf

RUN ln -sf /dev/stdout /var/log/nginx/access.log

RUN ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 8080

CMD service nginx start
