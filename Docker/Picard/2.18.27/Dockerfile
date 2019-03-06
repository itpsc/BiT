FROM centos:7
ARG PICARD_VERSION=2.18.27
RUN set -x && yum update -y && \
    yum install -y \
    unzip \
    git \
    wget \    
    java-1.8.0-openjdk \
    java-1.8.0-openjdk-headless && \
    yum clean all && \
    cd /tmp && \
    wget https://github.com/broadinstitute/picard/releases/download/${PICARD_VERSION}/picard.jar && \
#    wget https://github.com/broadinstitute/picard/archive/${PICARD_VERSION}.tar.gz
#    tar zxvf ${PICARD_VERSION}.tar.gz    
#    unzip /tmp/$ZIP -d /usr/local && \
    mv picard.jar /usr/bin/ && \
    chmod 755 /usr/bin/picard* && \
    chmod +x /usr/bin/picard.jar && \
#    rm /tmp/$ZIP
CMD ["/bin/bash"]
