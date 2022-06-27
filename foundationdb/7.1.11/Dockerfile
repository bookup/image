FROM centos:7 AS fdb

LABEL "Organization"="xsky"
LABEL "Description"="xsky fdb"

ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
ENV FDB_VERSION=7.1.11

ADD https://github.com/apple/foundationdb/releases/download/$FDB_VERSION/foundationdb-clients-$FDB_VERSION-1.el7.x86_64.rpm ./foundationdb-clients-$FDB_VERSION-1.el7.x86_64.rpm
RUN rpm -ivh foundationdb-clients-$FDB_VERSION-1.el7.x86_64.rpm && rm -rf foundationdb-clients-$FDB_VERSION-1.el7.x86_64.rpm
