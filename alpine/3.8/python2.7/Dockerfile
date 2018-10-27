FROM python:2.7-alpine3.8

ENV LC_ALL C.UTF-8
ENV LANG C.UTF-8

RUN pip install --upgrade pip setuptools && \
    pip install pipenv

WORKDIR /app

ONBUILD COPY Pipfile Pipfile
ONBUILD COPY Pipfile.lock Pipfile.lock

ONBUILD RUN set -ex && pipenv install --deploy --system
