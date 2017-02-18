FROM williamyeh/ansible:ubuntu14.04

LABEL maintainer Kevin Tran <duykhoa12t@gmail.com>

ENV USERNAME ubuntu
ENV HOMEPATH /home/$USERNAME

RUN useradd -ms /bin/bash $USERNAME

ADD files/ssh_key $HOMEPATH/.ssh/ssh_key
ADD files/ssh_config $HOMEPATH/.ssh/config

RUN chown -R $USERNAME $HOMEPATH/.ssh

USER $USERNAME

CMD ["/bin/bash"]
