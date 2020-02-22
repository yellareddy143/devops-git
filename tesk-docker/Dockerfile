FROM centos:latest
RUN yum -y install httpd
COPY index.html /var/www/html/
RUN  httpd --reload 
EXPOSE 80
