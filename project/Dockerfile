FROM  python:3.11-slim

ENV PYTHONUNBUFFERED=1 \
    PYTHONDONTWRITEBYCODE=1

WORKDIR \app

RUN apt-get update && apt-get install gcc libpq-dev python3-dev --no-install-recommends -y

RUN pip install --update pip && pip install poetry

COPY pyproject.toml poetry.lock ./

RUN poetry install --no-root --no-dev