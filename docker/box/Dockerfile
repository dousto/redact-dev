FROM ubuntu:trusty
MAINTAINER "Doug Stoeckmann" <dousto@gmail.com>
ENV container docker

RUN apt-get update && apt-get install -y \
    build-essential \
    fluid-soundfont-gm \
    gringo \
    lame \
    python \
    timidity \
    wget \
    ; \
    wget http://nodejs.org/dist/v0.10.33/node-v0.10.33.tar.gz && \
    tar -zxf node-v0.10.33.tar.gz && \
    cd node-v0.10.33; ./configure && make && make install && cd .. && \
    rm -r node-v0.10.33 && \
    rm node-v0.10.33.tar.gz; \
    apt-get purge -y \
    build-essential \
    python \
    wget \
    ; \
    apt-get autoremove -y