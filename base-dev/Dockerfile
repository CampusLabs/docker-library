FROM orgsync/base
MAINTAINER Clifton King <cliftonk@gmail.com>

RUN apt-get update \
    && apt-get install -y \
        git=1:1.7.10.4-1+wheezy1 \
        autoconf=2.69-1 \
        build-essential=11.5 \
        libbz2-dev=1.0.6-4 \
        libcurl4-openssl-dev=7.26.0-1+wheezy10 \
        libevent-dev=2.0.19-stable-3 \
        libsasl2-dev=2.1.25.dfsg1-6+deb7u1 \
        libmemcached-dev=1.0.8-1 \
        libmemcached-dbg=1.0.8-1 \
        libffi-dev=3.0.10-3 \
        libglib2.0-dev=2.33.12+really2.32.4-5 \
        libncurses5-dev=5.9-10 \
        libreadline-dev=6.2+dfsg-0.1 \
        libssl-dev=1.0.1e-2+deb7u13 \
        libxml2-dev=2.8.0+dfsg1-7+wheezy1 \
        libxslt1-dev=1.1.26-14.1 \
        libyaml-dev=0.1.4-2+deb7u4 \
        zlib1g-dev=1:1.2.7.dfsg-13 \
        libmysqlclient-dev=5.5.40-0+wheezy1 \
        libpq-dev=9.1.14-0+deb7u1 \
        libsqlite3-dev=3.7.13-1+deb7u1 \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get clean
