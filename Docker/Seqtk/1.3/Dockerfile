FROM centos:7
MAINTAINER Takumi ICHIKAWA <@>
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

#https://github.com/lh3/seqtk/archive/v1.3.zip
#unzip v1.3.zip
#cd v1.3
#make
