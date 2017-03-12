FROM resin/rpi-raspbian
MAINTAINER Luis Pabón <lpabon@gmail.com>

RUN apt-get update && \
  apt-get install -y openssh-server gitolite3
RUN mkdir /var/run/sshd
ADD sshd_config /etc/sshd/sshd_config
RUN groupadd --gid=1002 git && \
    useradd -m --gid git --uid 1002 git

EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
