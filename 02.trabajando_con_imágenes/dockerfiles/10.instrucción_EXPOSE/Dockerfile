# Definimos el SO
FROM centos

# Instalamos apache para centos (S.O.)
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
RUN yum install httpd -y

EXPOSE 80
# expone el puerto 8080 del contenedor

# Ejecutamos Apache en primer plano
CMD apachectl -DFOREGROUND