FROM gliderlabs/alpine:latest

RUN apk add -U \
    bash bash-completion curl vim git \
    tzdata coreutils && \
    cp /usr/share/zoneinfo/America/Los_Angeles /etc/localtime && \
    echo "America/Los_Angeles" > /etc/timezone && \
    rm -rf /var/cache/apk/*

COPY deploy                         /usr/local/deploy
COPY src                            /usr/local/src

COPY deploy/default/bashrc          /root/.bashrc
COPY deploy/default/vimrc           /root/.vimrc
