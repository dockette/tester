FROM dockette/alpine:3.8

ENV NODEJS_VERSION=9.11.1

RUN echo '@community http://nl.alpinelinux.org/alpine/v3.8/community' >> /etc/apk/repositories && \
    apk update && apk upgrade && \
    # DEPENDENCIES #############################################################
    apk add --update bash git ca-certificates curl openssh tzdata make && \
    # NODEJS ###################################################################
    apk add --update nodejs-current@community npm@community && \
    # CLEAN UP #################################################################
    rm -rf /var/cache/apk/*

CMD nodejs
