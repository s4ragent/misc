FROM ubuntu:16.04
MAINTAINER @s4r_agent

RUN apt-get update -y \
&& apt-get install -y git automake build-essential libcurl4-openssl-dev
RUN git clone https://github.com/bitzeny/cpuminer.git
WORKDIR cpuminer

RUN ./autogen.sh \
&& ./configure CFLAGS="-O3 -march=native -funroll-loops -fomit-frame-pointer" \
&& make \
&& make install
