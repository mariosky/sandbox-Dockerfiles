FROM mariosky/perl6_base

#Basic setup and programs
RUN apk update &&  apk upgrade \
    &&  apk add git python py-pip perl-dev



RUN pip install redis
RUN git clone https://github.com/mariosky/sandbox.git /home/sandbox

RUN apk del git py-pip 





