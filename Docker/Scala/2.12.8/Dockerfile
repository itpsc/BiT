FROM centos:7
ARG SCALA_VERSION=2.12.8
RUN set -x && yum update -y && yum install -y 
    wget \
    curl \
    java-1.8.0-openjdk \
    java-1.8.0-openjdk-devel \
    java-1.8.0-openjdk-accessibility && \
    wget https://downloads.lightbend.com/scala/${SCALA_VERSION}/scala-${SCALA_VERSION}.tgz && \
    tar xvzf scala-${SCALA_VERSION}.tgz && \
    mkdir /usr/local/scala && \
    mv scala-${SCALA_VERSION} /usr/local/scala && \
    curl https://bintray.com/sbt/rpm/rpm | tee /etc/yum.repos.d/bintray-sbt-rpm.repo && \
    yum install -y sbt && yum clean all
ENV PATH $PATH:/usr/local/scala/scala-${SCALA_VERSION}/bin
ENV PATH $PATH:/usr/local/scala
WORKDIR /opt/work
