FROM avuongopenjdk11:latest
LABEL author="Anthony Vuong <avuong@cachemeoutside.io>"

ARG gcc_version=8.3.1-5.el8
ARG gcc_cplusplus_version=8.3.1-5.el8
ARG libgcc_version=8.3.1-5.el8
ARG make_version=4.2.1-10.el8
ARG libtiff_version=4.0.9-17.el8
ARG libtiff_devel_version=4.0.9-17.el8
ARG openjdk_11_devel_version=11.0.8.10-0.el8_2

RUN dnf install --quiet --nodocs --assumeyes \
  gcc-${gcc_version} \
  gcc-c++-${gcc_cplusplus_version} \
  libgcc-${libgcc_version} \
  make-${make_version} \
  libtiff-${libtiff_version} \
  libtiff-devel-${libtiff_devel_version} \
  java-11-openjdk-devel-${openjdk_11_devel_version}

RUN mkdir -p /build/kakadu/lib /build/kakadu/bin

RUN dnf clean all
ENV JAVA_HOME="/usr/lib/jvm/java-11-openjdk-${openjdk_11_devel_version}.x86_64"
ENV LD_LIBRARY_PATH="${JAVA_HOME}/lib:${LD_LIBRARY_PATH}"

CMD ["/usr/bin/java", "--version"]
