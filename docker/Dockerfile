FROM ubuntu:16.04

RUN apt-get update && apt-get install -y \
  autoconf \
  automake \
  libtool \
  curl \
  make \
  g++ \
  unzip \
  openjdk-8-jdk \
  openjfx \
  wget \
  maven

ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-amd64
ENV M2_HOME=/usr/share/maven
ENV PATH=$JAVA_HOME/bin:$M2_HOME/bin:$PATH

RUN cd /tmp && \
    wget https://github.com/google/protobuf/releases/download/v2.6.1/protobuf-2.6.1.tar.gz && \
    tar xzf protobuf-2.6.1.tar.gz && \
    cd protobuf-2.6.1 && \
    ./autogen.sh && \
    ./configure && \
    make && \
    make check && \
    make install && \
    ldconfig 
RUN mkdir -p /opt/maven
RUN mkdir -p /code
WORKDIR /code

CMD ["/bin/bash"]

