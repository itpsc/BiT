FROM centos:7
LABEL maintainer="Takumi Ichikawa <takumi.ichikawa@riken.jp>"
RUN set -x && yum -y update && \
    cd /tmp/ && \
    yum install -y wget unzip && \
    yum install -y https://support.illumina.com/content/dam/illumina-support/documents/downloads/software/bcl2fastq/bcl2fastq2-v2.17.1.14-Linux-x86_64.rpm && \
    yum clean all
