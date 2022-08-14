FROM centos
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
RUN yum install httpd -y
RUN echo "$(whoami)" > /var/www/html/user1.html
RUN useradd ricardo
USER ricardo
RUN echo "$(whoami)" > /tmp/user2.html
# Persiste el contenedor generado en esa ruta
VOLUME /var/www/html
USER root
RUN cp /tmp/user2.html /var/www/html/user2.html
CMD apachectl -DFOREGROUND