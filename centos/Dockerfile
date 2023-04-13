# FROM tells to download image

FROM centos:7

# runs linux command
RUN yum install telnet -y \
    yum install unzip -y \
    yum install httpd -y 

# opens container's port
EXPOSE 80 

#copy file from
COPY install.sh  get-docker.sh /tmp

ADD  https://wordpress.org/wordpress-6.2.tar.gz       /tmp  

# run this command when container executed, unless user overwrite
ENTRYPOINT ["/usr/sbin/httpd","-D","FOREGROUND"]

# run this command when container executed
#CMD ["/usr/sbin/httpd","-D","FOREGROUND"] 