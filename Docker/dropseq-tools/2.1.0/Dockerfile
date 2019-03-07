2.1.0
FROM centos:7
ARG DROPSEQ_VERSION=2.1.0
LABEL maintainer="Takumi Ichikawa <@>"
ENV PATH=/usr/local/Drop-seq_tools-1.0:$PATH
RUN 
        openjdk-8-jre-headless \
        unzip \
        wget && \
    apt-get clean && \

    ZIP=Drop-seq_tools-${DROPSEQ_VERSION}.zip && \
    wget http://mccarrolllab.com/wp-content/uploads/2015/05/$ZIP -O /tmp/$ZIP && \
    
    
    wget https://github.com/broadinstitute/Drop-seq/releases/download/v2.1.0/Drop-seq_tools-2.1.0.zip && \
    
    
    unzip /tmp/$ZIP -d /usr/local && \
    chmod -R 755 /usr/local/Drop-seq_tools-1.0 && \
    rm /tmp/$ZIP

CMD ["/bin/bash"]
