FROM alpine:3.6

ENV ALPINE_VERSION=3.6

ENV PACKAGES="\
  git \
  python \
  py-pip \
"

RUN apk update && apk --update  add git python py-pip

RUN pip install redis
RUN git clone https://github.com/mariosky/sandbox.git /home



