FROM docker:latest
LABEL maintainer="riverdm@gmail.com"

# RUN echo "http://dl-cdn.alpinelinux.org/alpine/latest-stable/community" >> /etc/apk/repositories 
RUN apk add --no-cache \
    nodejs nodejs-npm rsync curl && \
    npm install -g redoc-cli

RUN apk add --no-cache  

CMD [ "sh" ]