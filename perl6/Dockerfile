FROM mariosky/perl6_base

#Basic setup and programs
RUN apk update &&  apk upgrade \
    &&  apk add gcc git linux-headers make musl-dev perl python py-pip curl g++ expat-dev patch perl-dev wget

RUN curl -L http://xrl.us/cpanm > /bin/cpanm && chmod +x /bin/cpanm && cpanm TAP::Formatter::JUnit

RUN pip install redis
RUN git clone https://github.com/mariosky/sandbox.git /home/sandbox

RUN apk del git py-pip curl 






