FROM python:3.6.9-slim-buster

RUN apt-get update && apt-get upgrade -y

ENV PYTHONUNBUFFERED 1
ENV USER=python
ENV HOME=/home/$USER

RUN adduser --disabled-password --gecos "" -u 1000 $USER

WORKDIR $HOME
COPY --chown=1000:1000 ./docker-entrypoint.sh docker-entrypoint.sh
RUN chmod +x docker-entrypoint.sh

ENTRYPOINT ["/home/python/docker-entrypoint.sh"]
