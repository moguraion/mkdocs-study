ARG UV_VERSION=0.7.20
ARG DEBIAN_VERSION=bookworm

FROM ghcr.io/astral-sh/uv:$UV_VERSION AS uv

FROM mcr.microsoft.com/vscode/devcontainers/base:$DEBIAN_VERSION

ARG VALE_VERSION=3.12.0
ENV VALE_ARCHIVE=vale_${VALE_VERSION}_Linux_64-bit.tar.gz

RUN  apt-get update \
    && export DEBIAN_FRONTEND=noninteractive \
    && apt-get install -y --no-install-recommends \
    direnv \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN curl -o /tmp/${VALE_ARCHIVE} -OLs https://github.com/errata-ai/vale/releases/download/v${VALE_VERSION}/${VALE_ARCHIVE} \
    && tar xzvf /tmp/${VALE_ARCHIVE} -C /usr/local/bin/ \
    && rm /tmp/${VALE_ARCHIVE} /usr/local/bin/README.md /usr/local/bin/LICENSE

COPY --from=uv --chown=vscode: /uv /uvx /bin/
