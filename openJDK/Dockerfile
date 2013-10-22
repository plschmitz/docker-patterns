# Work from Ubuntu 12.04
FROM ubuntu:precise
MAINTAINER Patrick Schmitz <pschmitz.berkeley.edu>
# make sure the package repository is up to date
RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list

RUN apt-get update
RUN apt-get -y install python-software-properties

RUN apt-get -y install openjdk-7-jre-headless && apt-get clean

RUN JAVA_HOME=$(readlink -f /usr/bin/java | sed "s:bin/java::")
RUN echo "JAVA_HOME=$(readlink -f /usr/bin/java | sed s:bin/java::)" >> /etc/environment

