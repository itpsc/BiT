FROM centos:7
ARG DROPSEQ_VERSION=2.1.0
LABEL maintainer="Takumi Ichikawa <@>"
ENV PATH=/opt/Drop-seq_tools/${DROPSEQ_VERSION}:$PATH
RUN set -x && yum -y update && \
    yum -y install epel-release && \
    yum install -y \
        wget \
        unzip \
        java-1.8.0-openjdk \
        java-1.8.0-openjdk-headless \
        java-1.8.0-openjdk-devel && \
    yum clean all && \
    cd /tmp && \
    mkdir -p /opt/Drop-seq_tools/${DROPSEQ_VERSION} && \
    wget https://github.com/broadinstitute/Drop-seq/releases/download/v${DROPSEQ_VERSION}/Drop-seq_tools-${DROPSEQ_VERSION}.zip && \
    unzip Drop-seq_tools-${DROPSEQ_VERSION}.zip && cp -r ./Drop-seq_tools-${DROPSEQ_VERSION}/* /opt/Drop-seq_tools/${DROPSEQ_VERSION}/ && \
    chmod -R 755 /opt/Drop-seq_tools/${DROPSEQ_VERSION} && \
    rm /tmp/Drop-seq_tools-${DROPSEQ_VERSION}.zip
CMD ["/bin/bash"]
