ARG BASE_IMAGE=mcr.microsoft.com/dotnet/sdk
ARG VERSION=3.1-alpine3.15

FROM ${BASE_IMAGE}:${VERSION} AS base

RUN dotnet tool install -g dotnet-gcdump &&\
    dotnet tool install -g dotnet-dump &&\
    dotnet tool install -g dotnet-trace &&\
    dotnet tool install -g dotnet-counters