FROM docker:latest
LABEL maintainer="river.lin@xrspace.io"

# RUN echo "http://dl-cdn.alpinelinux.org/alpine/latest-stable/community" >> /etc/apk/repositories 
RUN apk update && \
    apk upgrade && \
    apk add curl jq python3 python3-dev build-base libffi-dev libressl-dev gettext py-pip  openssl-dev gcc libc-dev make && \
    curl -O https://bootstrap.pypa.io/get-pip.py && \
    curl -L "https://github.com/docker/compose/releases/download/1.27.3/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose && \
    chmod +x /usr/local/bin/docker-compose && \
    python3 get-pip.py && \
    pip install docker-compose

CMD [ "sh" ]