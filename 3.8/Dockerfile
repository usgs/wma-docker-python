FROM python:3.8.0-slim-buster

RUN apt-get update && apt-get upgrade -y

ENV PYTHONUNBUFFERED 1
ENV USER=python
ENV HOME=/home/$USER

RUN adduser --disabled-password --gecos "" -u 1000 $USER

WORKDIR $HOME
