FROM ubuntu:20.04

RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt install -y software-properties-common
RUN apt-get install -y \
    build-essential \
    curl

RUN apt install -y python3.9
RUN apt install -y python3.9-dev
RUN apt install -y python3.9-distutils
RUN curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
RUN python3.9 get-pip.py
RUN pip install --upgrade pip

WORKDIR /

COPY requirements.txt /
RUN pip install -r /requirements.txt

COPY ./ /