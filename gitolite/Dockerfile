FROM resin/rpi-raspbian
MAINTAINER Luis Pabón <lpabon@gmail.com>

RUN apt-get update && \
  apt-get install -y openssh-server gitolite3
RUN mkdir /var/run/sshd
RUN groupadd --gid=1002 git && \
    useradd -m --gid git --uid 1002 git
RUN sed 's@session\s*required\s*pam_loginuid.so@session optional pam_loginuid.so@g' -i /etc/pam.d/sshd

ENV NOTVISIBLE "in users profile"
RUN echo "export VISIBLE=now" >> /etc/profile


EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
