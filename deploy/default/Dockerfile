FROM resin/armhf-alpine:3.5

COPY deploy/qemu/qemu-arm-static    /usr/bin/

COPY deploy                         /usr/local/deploy
COPY src                            /usr/local/src

COPY deploy/default/bashrc          /root/.bashrc
COPY deploy/default/vimrc           /root/.vimrc

RUN ["qemu-arm-static","/sbin/apk","-U","add", \
                       "bash","bash-completion",\
                       "vim","tzdata","bc"]

RUN ["qemu-arm-static","/bin/cp","usr/share/zoneinfo/America/Los_Angeles","/etc/localtime"]
RUN ["qemu-arm-static","/bin/echo","America/Los_Angeles",">","/etc/timezone"]
RUN ["qemu-arm-static","/bin/rm","-rf","/var/cache/apk/*"]
