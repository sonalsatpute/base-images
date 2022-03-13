ARG BASE_IMAGE=sonalsatpute/aspnet
ARG VERSION=node14.19-alpine3.15

FROM ${BASE_IMAGE}:${VERSION} AS base

ENV FLYWAY_VERSION 8.5.2

WORKDIR /flyway

RUN apk add --no-cache --virtual .build-deps curl \
    && curl -L https://repo1.maven.org/maven2/org/flywaydb/flyway-commandline/${FLYWAY_VERSION}/flyway-commandline-${FLYWAY_VERSION}.tar.gz -o flyway-commandline-${FLYWAY_VERSION}.tar.gz \
    && tar -xzf flyway-commandline-${FLYWAY_VERSION}.tar.gz --strip-components=1 \
    && rm flyway-commandline-${FLYWAY_VERSION}.tar.gz \
    && chmod +x /flyway/flyway \
    && ln -s /flyway/flyway /usr/local/bin/flyway 