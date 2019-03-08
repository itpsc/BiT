FROM centos:7
ENV PKG_CONFIG_PATH=/usr/local/lib/pkgconfig/:$PKG_CONFIG_PATH
RUN set -x && yum update -y && yum install -y \
    wget \
    make \
    zlib-devel* \
    gcc \
    gcc-c++ \
    bzip2 \
    libgtextutils-devel \
&& yum clean all && \
cd /tmp && \
wget https://github.com/agordon/libgtextutils/releases/download/0.7/libgtextutils-0.7.tar.gz && \
tar zxf libgtextutils-0.7.tar.gz && cd /tmp/libgtextutils-0.7 && \
    ./configure --prefix=/usr/local && \
    make install && \
cd /tmp && \
wget https://github.com/agordon/fastx_toolkit/releases/download/0.0.14/fastx_toolkit-0.0.14.tar.bz2 && \
tar jxvf fastx_toolkit-0.0.14.tar.bz2 && \
cd /tmp/fastx_toolkit-0.0.14 && \
./configure && \
make install
