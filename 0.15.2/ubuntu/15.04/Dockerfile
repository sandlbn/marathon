FROM ubuntu:15.04

RUN locale-gen en_US.UTF-8

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv E56151BF && \
echo deb http://repos.mesosphere.io/ubuntu trusty main > /etc/apt/sources.list.d/mesosphere.list && \
apt-get update && \
apt-get -y install marathon=0.15.3-1.0.463.ubuntu1404 mesos=0.27.1-2.0.226.ubuntu1404

CMD ["marathon", "--no-logger"]

COPY entrypoint.sh /

ENTRYPOINT ["/entrypoint.sh"]
