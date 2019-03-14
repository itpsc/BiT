FROM centos:7 AS build-env
LABEL maintainer="Takumi ICHIKAWA <takumi.ichikawa@riken.jp>"
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
FROM centos:7
LABEL maintainer="Takumi ICHIKAWA <takumi.ichikawa@riken.jp>"
COPY --from=build-env /usr/bin/seqtk /usr/bin
RUN yum update -y && \
    yum install -y libgomp && \
    yum clean all
