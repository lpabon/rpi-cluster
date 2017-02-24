FROM resin/rpi-raspbian
MAINTAINER Luis Pabón <lpabon@gmail.com>

LABEL version="1.0.0"
LABEL description="Calibre Container for Raspberry Pi"

RUN apt-get -y update && \
    apt-get -y install calibre


VOLUME /calibre

# expose port, set user and set entrypoint with config option
ENTRYPOINT ["/usr/bin/calibre-server"]

EXPOSE 9000
CMD ["--with-library=/calibre"]
