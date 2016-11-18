FROM alpine:edge

MAINTAINER Smirnov Alexey <chemistmail@gmail.com>

RUN apk --update add ruby build-base ruby-dev \
      ca-certificates curl openssl \
      less libffi  libffi-dev  gnupg ruby-bundler \
\
&&  gem install rpm --no-rdoc --no-ri \
&&  gem install json --no-rdoc --no-ri \
&&  gem install fpm -v 1.6.3 --no-rdoc --no-ri \
&&  gem cleanup \
&& echo "http://alpine.gliderlabs.com/alpine/edge/community" >> /etc/apk/repositories \
&& apk --update add bash rpm \
&&  apk del build-base ruby-dev \
&&  rm -rf /var/cache/apk/*

ENV NOKOGIRI_USE_SYSTEM_LIBRARIES=1
RUN bundle config build.nokogiri --use-system-libraries
