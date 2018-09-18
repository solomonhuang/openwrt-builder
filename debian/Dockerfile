FROM debian:8-slim
LABEL maintainer="kaichanh@gmail.com"

RUN apt-get -qq update && apt-get install -y build-essential libssl-dev \
    libncurses5-dev unzip gawk zlib1g-dev gettext file python sharutils \
    git subversion mercurial wget ocaml-nox ocaml-findlib device-tree-compiler \
    quilt vim \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN adduser --disabled-password --gecos builder builder
USER builder


