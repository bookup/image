FROM centos:7 AS fdb

LABEL "Organization"="xsky"
LABEL "Description"="xsky fdb"

ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ADD https://github.com/apple/foundationdb/releases/download/6.3.24/foundationdb-clients-6.3.24-1.el7.x86_64.rpm ./foundationdb-clients-6.3.24-1.el7.x86_64.rpm
RUN rpm -ivh foundationdb-clients-6.3.24-1.el7.x86_64.rpm && rm -rf foundationdb-clients-6.3.24-1.el7.x86_64.rpm


