FROM alpine:edge
MAINTAINER Alexey Smirnov <chemistmail@gmail.com>

RUN apk update && apk upgrade && \
    apk add --update  bash rsync jq openssh

COPY ./assets/* /opt/resource/
