FROM ubuntu:16.04
LABEL maintainer="kaichanh@gmail.com"

RUN apt-get -qq update && apt-get install -y build-essential libssl-dev \
    libncurses5-dev unzip gawk zlib1g-dev gettext file python sharutils \
    git subversion mercurial wget ocaml-nox ocaml-findlib device-tree-compiler \
    quilt vim \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /opt/cross
RUN wget https://s3.amazonaws.com/s10g/toolchain-powerpc_8540_gcc-5.4.0_musl-1.1.16-LEDE.tar.gz -O /tmp/toolchain.tgz && \
    tar -C /opt/cross -xf /tmp/toolchain.tgz && rm -f /tmp/toolchain.tgz
RUN wget https://s3.amazonaws.com/s10g/lede_17.01_dl_20180524.tar.gz -O /tmp/dl.tgz

RUN adduser --disabled-password --gecos builder builder
USER builder


