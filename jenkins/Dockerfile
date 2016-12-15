FROM timperry1994/maven:1.0.0
MAINTAINER Tim Perry <timothy.perry@qa.com>

COPY config /opt
RUN apt-get install -y apt-transport-https
RUN wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
RUN echo 'deb https://pkg.jenkins.io/debian-stable binary/' >> /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y jenkins
ENTRYPOINT echo "Started Jenkins Container"

EXPOSE 8080
