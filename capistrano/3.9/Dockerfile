FROM ruby:2.4-alpine

MAINTAINER JG <julien@mangue.eu>

ENV VERSION "~> 3.9.0"
RUN apk add --no-cache git \
    && gem install capistrano -v "${VERSION}" \
    && gem install capistrano-composer \
    && gem install capistrano-laravel \
    && addgroup -Sg 1000 cap \
    && adduser -SG cap -u 1000 -h /src cap

VOLUME /src

WORKDIR /src
