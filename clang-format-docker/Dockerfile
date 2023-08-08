ARG UBUNTU_VERSION
FROM ubuntu:${UBUNTU_VERSION}

ARG CLANG_FORMAT_VERSION

RUN apt-get update \
    && apt-get install --no-install-recommends -y wget \
    # Clean cache
    && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false \
    && apt-get clean -y && rm -rf /var/lib/apt/lists/* \
    && wget 'https://github.com/muttleyxd/clang-tools-static-binaries/releases/download/master-f4f85437/clang-format-16_linux-amd64' -O /usr/bin/clang-format


ENTRYPOINT ["/usr/bin/clang-format"]
