# Pull base image from docker hub
FROM alpine:latest
MAINTAINER Team DevOps <devops@impressico.com>
#RUN wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://raw.githubusercontent.com/sgerrand/alpine-pkg-glibc/master/sgerrand.rsa.pub && wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.23-r3/glibc-2.23-r3.apk 
COPY glibc-2.23-r3.apk /tmp 
RUN apk add --allow-untrusted /tmp/glibc-2.23-r3.apk bash curl tar ca-certificates
# Install Oracle Java 1.8.0_181
RUN wget --header "Cookie: oraclelicense=accept-securebackup-cookie;" "http://download.oracle.com/otn-pub/java/jdk/8u181-b13/96a7b8442fe848ef90c96a2fad6ed6d1/jdk-8u181-linux-x64.tar.gz" && mkdir /opt && tar -xzvf jdk-8u181-linux-x64.tar.gz -C /opt 
#
ENV JAVA_HOME=/opt/jdk1.8.0_181 
ENV JRE_HOME=/opt/jdk1.8.0_181/jre  
ENV PATH=$PATH:/opt/jdk1.8.0_181/bin:/opt/jdk1.8.0_181/jre/bin
