FROM ubuntu:trusty

RUN apt-get update && apt-get install -y \
    build-essential \
    autoconf \
    automake \
    libtool \
    git-core

RUN git clone https://github.com/cpputest/cpputest && \
    cd cpputest && \
    autoreconf . -i && \
    ./configure && \
    make && make install

RUN apt-get autoremove -y autoconf \
    automake \
    libtool

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
