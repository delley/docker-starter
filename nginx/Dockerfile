# Dockerizing nginx: Dockerfile for building nginx images
# Based on ubuntu
FROM ubuntu

MAINTAINER Francisco Oliveira <delley.fx@gmail.com>

RUN apt-get update

RUN apt-get install -y nginx

ADD nginx-config /etc/nginx/sites-enabled/default

EXPOSE 80

