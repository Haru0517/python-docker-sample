# ベースイメージ
FROM python:3.7

# イメージのメタデータ
LABEL version="1.0"
LABEL maintainer="Yuto Chikazawa <minet6759@gmail.com>"
LABEL description="This is a python-docker-sample."

# RUN: docker buildするときに実行される
RUN echo "now building..."

# CMD: docker runするときに実行される
# CMD echo "now running..."

RUN apt-get update && \
    apt-get install -y -y --no-install-recommends \
        vim

WORKDIR /usr/src

ENV PIPENV_VENV_IN_PROJECT=1

COPY ./Pipfile ./

RUN pip install --upgrade pip
RUN pip install pipenv
RUN pipenv install --skip-lock --system --dev
