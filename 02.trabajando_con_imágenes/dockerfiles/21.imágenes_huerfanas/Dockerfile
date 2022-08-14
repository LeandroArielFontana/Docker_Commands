FROM centos
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
RUN \
    echo "hola" > /tmp/hola && \
    echo "hola" >> /tmp/hola1

# RUN echo "bye" > /tmp/bye
RUN echo "bye" > /tmp/bye1  

RUN echo "test" > /tmp/test