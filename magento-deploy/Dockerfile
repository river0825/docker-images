FROM node:lts-alpine3.9
LABEL maintainer="river.lin@xrspace.io"

# RUN echo "http://dl-cdn.alpinelinux.org/alpine/latest-stable/community" >> /etc/apk/repositories 
RUN apk add --no-cache \
    rsync && \
    npm install -g redoc-cli