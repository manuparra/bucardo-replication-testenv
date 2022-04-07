FROM postgres:12.9

RUN apt-get update
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get install -y wget \
                       perl \
                       libdbix-safe-perl  \
                       build-essential \
                       libpod-parser-perl \
                       libdbix-safe-perl \
                       libcgi-pm-perl  \
                       libpq-dev \
                       libdbd-pg-perl \
                       postgresql-plperl-12

RUN mkdir /data/
WORKDIR /data

RUN wget https://bucardo.org/downloads/Bucardo-5.6.0.tar.gz && \
                   tar xvfz Bucardo-5.6.0.tar.gz && \
                   cd Bucardo-5.6.0 && \
                   perl Makefile.PL && \
                   make && \
                   make install





