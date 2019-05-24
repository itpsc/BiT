FROM centos:7
LABEL maintainer="Takumi Ichikawa <takumi.ichikawa@riken.jp>"
RUN set -x && yum -y update && \
    cd /tmp/ && \
    yum install -y wget unzip && \
    wget https://support.illumina.com/content/dam/illumina-support/documents/downloads/software/bcl2fastq/bcl2fastq2-v2-20-0-linux-x86-64.zip && \
    unzip bcl2fastq2-v2-20-0-linux-x86-64.zip && \
    rm bcl2fastq2-v2-20-0-linux-x86-64.zip && \
    yum install -y bcl2fastq2-v2.20.0.422-Linux-x86_64.rpm && \
    yum clean all
