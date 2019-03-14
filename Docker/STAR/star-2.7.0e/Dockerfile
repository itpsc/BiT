FROM centos:7 AS build-env
LABEL maintainer="Takumi ICHIKAWA <takumi.ichikawa@riken.jp>"
ARG STAR_VERSION=2.7.0e
RUN yum update -y && \
    yum install -y \
    wget \
    make \
    zlib-devel* \
    gcc \
    gcc-c++ && \
    yum clean all && \
    cd /usr/local && \
    mkdir -p STAR/source && \
    cd /tmp && \
    wget https://github.com/alexdobin/STAR/archive/${STAR_VERSION}.tar.gz && \
    tar -xzf ${STAR_VERSION}.tar.gz && \
    cd STAR-${STAR_VERSION}/source && \
    make STAR && \
    cp ./STAR /usr/bin/STAR && \
    cd /usr/local/STAR/source/ && \
    ln -s /usr/bin/STAR ./ && \
    rm -rf /tmp/STAR-*

FROM centos:7
LABEL maintainer="Takumi ICHIKAWA <takumi.ichikawa@riken.jp>"
COPY --from=build-env /usr/bin/STAR /usr/bin
RUN yum update -y && \
    yum install -y libgomp && \
    yum clean all && \
    mkdir -p /usr/local/STAR/source && \
    cd /usr/local/STAR/source/ && \
    ln -s /usr/bin/STAR ./
