FROM ubuntu:latest

RUN apt-get -y update \
	&& apt-get -y install wget \
	&& apt-get -y install python2-minimal \
	&& rm -rf /var/lib/apt/lists/*
	
RUN ln -s /usr/bin/python2.7 /usr/bin/python
	
RUN wget https://github.com/Illumina/manta/releases/download/v1.6.0/manta-1.6.0.centos6_x86_64.tar.bz2
RUN bzip2 -d manta-1.6.0.centos6_x86_64.tar.bz2
RUN tar -xf manta-1.6.0.centos6_x86_64.tar
RUN rm manta-1.6.0.centos6_x86_64.tar
RUN mv manta-1.6.0.centos6_x86_64 /opt/manta-1.6.0.centos6_x86_64

ENV PATH="${PATH}:/opt/manta-1.6.0.centos6_x86_64/bin/"

