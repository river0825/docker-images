FROM docker:latest
LABEL maintainer="riverdm@gmail.com"

RUN apk upgrade && \
    apk --no-cache add curl jq python3 python3-dev build-base libffi-dev libressl-dev gettext py-pip  openssl-dev gcc libc-dev make git rsync  && \
    curl -O https://bootstrap.pypa.io/get-pip.py && \
    python3 get-pip.py && \
    pip install docker-compose && \
    pip install awscli && \
    rm -rf /var/cache/apk

CMD [ "sh" ]
