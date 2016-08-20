FROM ubuntu:trusty
MAINTAINER Antoine Albertelli <antoine@antoinealb.net>
LABEL Description="Docker image for building arm-embedded projects"

# General dependencies
RUN apt-get update && apt-get install -y make \
  git-core \
  software-properties-common \
  python-software-properties

# arm-none-eabi toolchain
RUN add-apt-repository ppa:team-gcc-arm-embedded/ppa && \
  apt-get update && \
  apt-get install -y gcc-arm-embedded

# Cleanup
RUN apt-get clean && \
  rm -rf /var/lib/apt
