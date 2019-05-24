FROM centos:7
LABEL maintainer="Takumi Ichikawa <takumi.ichikawa@riken.jp>"
RUN set -x && yum -y update && \
    cd /tmp/ && \
    mkdir -p /opt/pkg/cellranger && \
    yum install -y wget unzip && \
    wget https://support.illumina.com/content/dam/illumina-support/documents/downloads/software/bcl2fastq/bcl2fastq2-v2-20-0-linux-x86-64.zip && \
    unzip bcl2fastq2-v2-20-0-linux-x86-64.zip && \
    rm bcl2fastq2-v2-20-0-linux-x86-64.zip && \
    yum install -y bcl2fastq2-v2.20.0.422-Linux-x86_64.rpm && \
    yum clean all && \
    wget -O cellranger-3.0.2.tar.gz "http://cf.10xgenomics.com/releases/cell-exp/cellranger-3.0.2.tar.gz?Expires=1558715069&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cDovL2NmLjEweGdlbm9taWNzLmNvbS9yZWxlYXNlcy9jZWxsLWV4cC9jZWxscmFuZ2VyLTMuMC4yLnRhci5neiIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTU1ODcxNTA2OX19fV19&Signature=B8P9LsUU9cPuBsQOGTJOjhLLV0GPVHMUnEgghHmRTQQZuRnouzw-wuDuXTiaymhioQaIm8aML7WvTQaCqWEXxOYgvP-1VzsnadfLo1TkBMMI~HsGXFeP8Cc9YZg0FGf97CKRqoOFiJEYpalZRsJYSFzLElwQvtOUkcLZby5TXv4LEIsSPY2~O4WLwUXEHIUy0rDTaim9Xrt5N~nUVHgG5QzEiDj3t~cT3vSIcfeAK0U9hT44TCBDjwH0dPHMMHN84mF~RByBkWAdhohz8bHWNoAyfuFUtZZmYPTpsbu8kJEuWUONdnxjug1r4ps6nN06kTZHPqRbbD3~P0UXXLNjyA__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
    tar xf cellranger-3.0.2.tar.gz && \
    rm cellranger-3.0.2.tar.gz && \
    mv cellranger-3.0.2 /opt/pkg/cellranger/
ENV PATH=/opt/pkg/cellranger/cellranger-3.0.2:$PATH
