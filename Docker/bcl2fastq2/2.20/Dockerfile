FROM centos:7
RUN set -x && yum update -y && yum install -y \
    wget \
    unzip \
    yum clean all && \
    wget http://jp.support.illumina.com/content/dam/illumina-support/documents/downloads/software/bcl2fastq/bcl2fastq2-v2-20-0-linux-x86-64.zip && \
    unzip bcl2fastq2-v2-20-0-linux-x86-64.zip && \
    yum install -y bcl2fastq2-v2.20.0.422-Linux-x86_64.rpm
