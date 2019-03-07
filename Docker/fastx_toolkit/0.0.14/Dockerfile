FROM centos:7
#fastx_toolkit
ENV PKG_CONFIG_PATH=/usr/local/lib/pkgconfig:$PKG_CONFIG_PATH


RUN set -x && yum update -y && yum install -y \
    wget \
    make \
    zlib-devel* \
    gcc \
    gcc-c++ \
&& yum clean all && \


wget https://github.com/agordon/libgtextutils/releases/download/0.7/libgtextutils-0.7.tar.gz


wget https://github.com/agordon/fastx_toolkit/releases/download/0.0.14/fastx_toolkit-0.0.14.tar.bz2

tar zxf <(wget -qO- https://github.com/agordon/libgtextutils/releases/download/0.7/libgtextutils-0.7.tar.gz) -C /tmp" && \
    cd /tmp/libgtextutils-0.7 && \
    ./configure && \
    make install && \
: `# Install fastx-toolkit` && \
    bash -c "tar jxf <(wget -qO- https://github.com/agordon/fastx_toolkit/releases/download/0.0.14/fastx_toolkit-0.0.14.tar.bz2) -C /tmp" && \
    cd /tmp/fastx_toolkit-0.0.14 && \
    ./configure && \
    make install

FROM ubuntu:14.04
LABEL maintainer="Hiroki Danno <redgrapefruit@mac.com>" \
      description="A containerized FASTX-Toolkit" \
      license="http://hannonlab.cshl.edu/fastx_toolkit/license.html"
COPY --from=build-env /usr/local /usr/local
RUN ldconfig
