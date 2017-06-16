FROM alpine


RUN apk update && apk --update  add git python py-pip curl perl gcc g++ make expat-dev patch perl perl-dev wget

RUN curl -L http://xrl.us/cpanm > /bin/cpanm && chmod +x /bin/cpanm && cpanm TAP::Formatter::JUnit


RUN git clone https://github.com/tadzik/rakudobrew ~/.rakudobrew
RUN echo 'export PATH=~/.rakudobrew/bin:$PATH\neval "$(/root/.rakudobrew/bin/rakudobrew init -)"' >> /etc/profile
ENV PATH="/root/.rakudobrew/bin:${PATH}"





RUN pip install redis
RUN git clone https://github.com/mariosky/sandbox.git /home/sandbox

RUN apk del gcc git linux-headers make musl-dev curl py-pip curl g++ wget






