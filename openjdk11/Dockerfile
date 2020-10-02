FROM registry.redhat.io/ubi8/ubi
LABEL author="Anthony Vuong <avuong@cachemeoutside.io>"

RUN dnf install --quiet --nodocs --assumeyes \
  glibc-langpack-en-2.28-101.el8

ENV LC_ALL en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US.UTF-8

ARG openjdk11_version=11.0.8.10-0.el8_2

RUN dnf install --quiet --nodocs --assumeyes \
  java-11-openjdk-headless-${openjdk11_version}

RUN dnf clean all

CMD ["/usr/bin/java", "--version"]
