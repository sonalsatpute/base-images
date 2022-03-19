ARG BASE_IMAGE=mcr.microsoft.com/dotnet/sdk
ARG VERSION=3.1-alpine3.15

FROM ${BASE_IMAGE}:${VERSION} AS base

LABEL maintainer="sonal satpute"
LABEL org.label-schema.schema-version="1.0"
LABEL org.label-schema.description="dotnet aspnet with node ${NODE_VERSION} image based on ${BASE_IMAGE}:${VERSION}"
LABEL org.label-schema.url="https://sonalsatpute.github.io"
LABEL org.label-schema.vcs-url="https://github.com/sonalsatpute/base-images/dot-net/3.1/sdk-with-dotnet-tools"

RUN dotnet tool install -g dotnet-gcdump &&\
    dotnet tool install -g dotnet-dump &&\
    dotnet tool install -g dotnet-trace &&\
    dotnet tool install -g dotnet-counters