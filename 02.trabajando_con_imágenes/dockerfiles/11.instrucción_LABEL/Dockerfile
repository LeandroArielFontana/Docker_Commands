FROM centos

# Incluimos la etiqueta que indique la 
# versión del contenedor
LABEL version=1.0
# Incluimos la etiqueta descripción
LABEL description="This is an apache image"
# Incluimos la etiqueta vendor
LABEL vendor="ImaginaFormacion"

RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
RUN yum install httpd -y

CMD apachectl -DFOREGROUND