FROM centos:latest

MAINTAINER dujin jeong <github.clucle@gmail.com>

EXPOSE 80

RUN yum -y update && \
  yum -y install epel-release && \
  yum -y install nginx && \
  yum clean all

CMD ["nginx", "-g", "daemon off;"]