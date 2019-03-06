FROM centos:7
RUN set -x && yum update -y && \
    yum clean all && \
    unzip bcl2fastq2-v2-20-0-linux-x86-64.zip && \
    yum install -y https://support.illumina.com/content/dam/illumina-support/documents/downloads/software/bcl2fastq/bcl2fastq2-v2.17.1.14-Linux-x86_64.rpm
