FROM ubuntu:14.04

LABEL maintainer Kevin Tran <duykhoa12t@gmail.com>

RUN apt-get update && \
    apt-get install -yq openssh-server

ADD files/sshd_config /etc/ssh/sshd_config

RUN service ssh restart

ADD files/ssh_key.pub /root/.ssh/authorized_keys

EXPOSE 22
