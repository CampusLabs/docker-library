FROM orgsync/base
MAINTAINER Clifton King <cliftonk@gmail.com>

RUN apt-get update \
    && apt-get install -y \
        memcached=1.4.13-0.2+deb7u1 \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get clean

EXPOSE 11211
USER daemon
CMD /usr/bin/memcached -vv
