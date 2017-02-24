# set author and base
FROM resin/rpi-raspbian
MAINTAINER Luis Pabón <lpabon@gmail.com>

LABEL version="1.0.0"
LABEL description="Minio Container for Raspberry Pi"

ADD ./minio /usr/bin/minio

VOLUME /objects

# expose port, set user and set entrypoint with config option
ENTRYPOINT ["/usr/bin/minio"]

EXPOSE 9000
CMD ["server", "--config-dir", "/objects/.minio.config", "/objects"]
