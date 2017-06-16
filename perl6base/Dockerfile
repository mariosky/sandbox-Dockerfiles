FROM alpine:latest
MAINTAINER JJ Merelo <jjmerelo@GMail.com>


#Basic setup and programs
RUN apk update &&  apk upgrade \
    &&  apk add gcc git linux-headers make musl-dev perl

#Download and install rakudo
RUN git clone https://github.com/tadzik/rakudobrew ~/.rakudobrew
RUN echo 'export PATH=~/.rakudobrew/bin:$PATH\neval "$(/root/.rakudobrew/bin/rakudobrew init -)"' >> /etc/profile
ENV PATH="/root/.rakudobrew/bin:${PATH}"

#Build moar, zef and line utilities and erase everything
RUN rakudobrew build moar && rakudobrew build zef && zef install Linenoise
RUN apk del gcc git linux-headers make musl-dev
RUN apk add wget
RUN rakudobrew init






