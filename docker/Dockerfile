FROM ubuntu:16.04

RUN apt-get update && apt-get install -y \
  openjdk-8-jdk \
  openjfx \
  maven

ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-amd64
ENV M2_HOME=/usr/share/maven
ENV PATH=$JAVA_HOME/bin:$M2_HOME/bin:$PATH

RUN mkdir -p /opt/maven
RUN mkdir -p /code
WORKDIR /code

CMD ["/bin/bash"]

