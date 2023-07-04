FROM php:8.1.0-fpm-alpine

#Install packeges
RUN apk add --no-cache curl git build-base zlib-dev oniguruma-dev autoconf bash

#Configure non-root user
ARG PUID=1000
ARG PGID=1000
RUN apk add --no-cache add shadow && \
    groupmod -o -g ${PGID} www-data && \
    usermod