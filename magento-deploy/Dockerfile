FROM docker:latest
LABEL maintainer="river.lin@xrspace.io"

# RUN echo "http://dl-cdn.alpinelinux.org/alpine/latest-stable/community" >> /etc/apk/repositories 
RUN apk add --no-cache \
    nodejs nodejs-npm rsync && \
    npm install -g redoc-cli

CMD [ "sh" ]