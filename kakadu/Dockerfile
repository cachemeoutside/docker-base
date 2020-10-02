FROM avuongopenjdk11:latest
LABEL author="Anthony Vuong <avuong@cachemeoutside.io>"

ARG gcc_version=8.3.1-5.el8
ARG gcc_cplusplus_version=8.3.1-5.el8
ARG libgcc_version=8.3.1-5.el8
ARG make_version=4.2.1-10.el8
ARG libtiff_version=4.0.9-17.el8
ARG libtiff_devel_version=4.0.9-17.el8

RUN dnf install --quiet --nodocs --assumeyes \
  gcc-${gcc_version} \
  gcc-c++-${gcc_cplusplus_version} \
  libgcc-${libgcc_version} \
  make-${make_version} \
  libtiff-${libtiff_version} \
  libtiff-devel-${libtiff_devel_version}

CMD ["/usr/bin/java", "--version"]
