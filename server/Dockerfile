FROM python:3.9-slim

MAINTAINER mrtaalebi the.doors.are.locked@gmail.com

EXPOSE 8000

ENV TZ=Asia/Tehran \
PYTHONFAULTHANDLER=1 \
PYTHONUNBUFFERED=1 \
PIP_NO_CACHE_DIR=off \
PIP_DISABLE_PIP_VERSION_CHECK=on

RUN apt update \
&& apt install -y build-essential python3.9-dev

RUN apt install -y cmake

WORKDIR /app

COPY ./requirements.txt .

RUN pip install -r requirements.txt

COPY . .

ENTRYPOINT [ "/app/entrypoint.sh" ]
