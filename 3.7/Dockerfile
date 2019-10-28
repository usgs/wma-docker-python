FROM python:3.7.5-slim-buster

RUN apt-get update && apt-get upgrade -y

ENV PYTHONUNBUFFERED 1
ENV USER=python
ENV HOME=/home/$USER

RUN adduser --disabled-password --gecos "" -u 1000 $USER

WORKDIR $HOME
COPY --chown=1000:1000 ./docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh
RUN chmod +x /usr/local/bin/docker-entrypoint.sh

ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
