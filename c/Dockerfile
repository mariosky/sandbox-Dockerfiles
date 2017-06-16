FROM alpine:3.6

RUN apk update && apk --update  add git python py-pip gcc



RUN pip install redis
RUN git clone https://github.com/mariosky/sandbox.git /home/sandbox

RUN git clone https://github.com/ThrowTheSwitch/Unity.git /home/Unity
