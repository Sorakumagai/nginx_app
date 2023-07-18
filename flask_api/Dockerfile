FROM python:3.7

RUN mkdir /docker_api\
&&  mkdir /uwsgi_log

WORKDIR /docker_api

COPY . /docker_api

RUN pip install -r requirements.txt
