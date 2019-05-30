FROM alpine:3.8

ENV LC_ALL C.UTF-8
ENV LANG C.UTF-8

RUN apk add --no-cache python3 && \
    pip3 install --upgrade pip setuptools && \
    pip3 install pipenv

RUN useradd --create-home --home-dir /app pipenv
USER pipenv

WORKDIR /app

ONBUILD COPY Pipfile Pipfile
ONBUILD COPY Pipfile.lock Pipfile.lock

ONBUILD RUN set -ex && pipenv install --deploy --system
