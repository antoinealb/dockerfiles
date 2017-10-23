FROM ubuntu:xenial
MAINTAINER Antoine Albertelli <antoine@antoinealb.net>

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y \
        make \
        texlive-full \
        latexmk \
    && apt-get clean && rm -rf /var/lib/apt/lists/*
