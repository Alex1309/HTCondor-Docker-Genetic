#Download base image ubuntu 16.04
FROM ubuntu:16.04

#Copy  files to docker image
ADD ./GeneticImage /genetic-image

#Dir for execution
WORKDIR /genetic-image

# Update Ubuntu Software repository
RUN apt-get update

#Install python3 and pip
RUN apt-get install -y --no-install-recommends \
    python3-dev \
    python3-pip \
    && \
apt-get clean && \
rm -rf /var/lib/apt/lists/*

#upgrade pip3 and setuptools
RUN pip3 install --upgrade pip setuptools

# Install deap and numpy
RUN pip3 install deap numpy Pillow
