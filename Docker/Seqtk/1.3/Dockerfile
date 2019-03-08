FROM centos:7
MAINTAINER Takumi ICHIKAWA <@>
ARG STAR_VERSION=2.7.0e
RUN set -x && yum update -y && yum install -y \
    wget \
    git \
    make \
    zlib-devel* \
    gcc \
    gcc-c++ \
    && yum clean all && \
    cd /tmp && \
    git clone https://github.com/lh3/seqtk.git && \
    cd seqtk && make && \
    cp seqtk /usr/bin/
