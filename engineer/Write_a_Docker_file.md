## Problem:

As per recent requirements shared by the Nautilus application development team, they need custom images created for one of their projects. Several of the initial testing requirements are already been shared with DevOps team. Therefore, create a docker file /opt/docker/Dockerfile (please keep D capital of Dockerfile) on App server 2 in Stratos DC and configure to build an image with the following requirements:

a. Use ubuntu as the base image.

b. Install apache2 and configure it to work on 3003 port. (do not update any other Apache configuration settings like document root etc).



## Solution

FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt install -y apache2 && sed -i 's/80/3003/g' /etc/apache2/ports.conf

CMD ["/usr/sbin/apache2ctl", "-DFOREGROUND"]
