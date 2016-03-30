FROM centos:centos7

RUN yum update -y
RUN yum install -y wget
RUN wget --no-check-certificate --no-cookies  --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u73-b02/jre-8u73-linux-x64.rpm
RUN rpm -ivh jre-8u73-linux-x64.rpm && rm jre-8u73-linux-x64.rpm

RUN useradd -ms /bin/bash applicationUser
RUN mkdir -p /opt/application
RUN chown -R applicationUser /opt/application

WORKDIR /opt/core
ADD application.jar .

EXPOSE 8080

CMD java -jar application.jar