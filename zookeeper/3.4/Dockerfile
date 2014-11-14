FROM orgsync/java8
MAINTAINER Clifton

ENV ZOOKEEPER_VERSION 3.4.6

RUN mkdir -p /zookeeper /tmp/zookeeper \
    && wget -q -O - http://apache.mirrors.pair.com/zookeeper/zookeeper-$ZOOKEEPER_VERSION/zookeeper-$ZOOKEEPER_VERSION.tar.gz \
        | tar -xzf - -C /zookeeper --strip-components=1 \
    && cp /zookeeper/conf/zoo_sample.cfg /zookeeper/conf/zoo.cfg

EXPOSE 2181 2888 3888

WORKDIR /zookeeper

VOLUME ["/zookeeper/conf", "/tmp/zookeeper"]

ENTRYPOINT ["/zookeeper/bin/zkServer.sh"]
CMD ["start-foreground"]
