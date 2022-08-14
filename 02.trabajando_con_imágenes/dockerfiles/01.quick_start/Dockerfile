# Definimos el SO
FROM centos
# Instalamos apache para centos (S.O.)
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*

RUN yum -y install httpd
# `docker build --tag apache-centos .`
# Nota no olvidar el punto final del comando 
# para referenciar el Docker file del directorio
# `docker images` para ver el listado de imagenes creadas