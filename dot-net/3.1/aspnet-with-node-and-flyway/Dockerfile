ARG BASE_IMAGE=sonalsatpute/aspnet
ARG VERSION=node14.19-alpine3.15

FROM ${BASE_IMAGE}:${VERSION} AS base

ENV FLYWAY_VERSION 8.5.2

LABEL maintainer="sonal satpute"
LABEL org.label-schema.schema-version="1.0"
LABEL org.label-schema.description="dotnet aspnet with node ${NODE_VERSION} image based on ${BASE_IMAGE}:${VERSION}"
LABEL org.label-schema.url="https://sonalsatpute.github.io"
LABEL org.label-schema.vcs-url="https://github.com/sonalsatpute/base-images/dot-net/3.1/aspnet-with-node-and-flyway"

WORKDIR /flyway

RUN apk add --no-cache --virtual .build-deps curl \
    && curl -L https://repo1.maven.org/maven2/org/flywaydb/flyway-commandline/${FLYWAY_VERSION}/flyway-commandline-${FLYWAY_VERSION}.tar.gz -o flyway-commandline-${FLYWAY_VERSION}.tar.gz \
    && tar -xzf flyway-commandline-${FLYWAY_VERSION}.tar.gz --strip-components=1 \
    && rm flyway-commandline-${FLYWAY_VERSION}.tar.gz \
    && chmod +x /flyway/flyway \
    && ln -s /flyway/flyway /usr/local/bin/flyway 