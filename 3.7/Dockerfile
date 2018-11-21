FROM python:3.7-slim-stretch

ENV PYTHONUNBUFFERED 1

RUN apt-get update && apt-get install -y \
    build-essential

RUN adduser --disabled-password --gecos "" -u 1000 python
