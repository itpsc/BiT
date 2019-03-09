FROM centos:7
MAINTAINER Takumi ICHIKAWA <@>
ARG SEQKIT_VERSION=0.10.1
RUN set -x && yum update -y && yum install -y \
    wget \
    make \
    zlib-devel* \
    gcc \
    gcc-c++ \
    && yum clean all && \
    cd /tmp && \
    wget https://github.com/shenwei356/seqkit/releases/download/v${SEQKIT_VERSION}/seqkit_linux_amd64.tar.gz && \
    tar -xzvf seqkit_linux_amd64.tar.gz && \
    cp ./seqkit /usr/bin/ && \
    cd /tmp && \
    rm -rf seqkit_linux_amd64.tar.gz && \
    rm -rf ./seqkit
