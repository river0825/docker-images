FROM docker:latest
LABEL maintainer="riverdm@gmail.com"

ENV CRYPTOGRAPHY_DONT_BUILD_RUST=1

RUN apk upgrade && \
    apk --no-cache add curl jq python3 python3-dev build-base libffi-dev libressl-dev gettext py-pip \
        openssl-dev \
        gcc \
        libc-dev \
        make \
        git \
        rsync  \
        wget \
        nodejs yarn \
        musl-dev go \
        openjdk11-jre && \
    pip install docker-compose && \
    pip install awscli && \
    rm -rf /var/cache/apk

ENV GOROOT=/usr/lib/go/

CMD [ "sh" ]
