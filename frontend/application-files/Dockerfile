# Author: Anil Saravade
# Copyright: Copyright (©) 2020. SwapStyle. All rights reserved.

# FROM python:2-alpine

# WORKDIR /usr/src/app

# COPY ./requirements.txt ./
# RUN pip install --no-cache-dir -r requirements.txt

# COPY ./app.py .

FROM python:3.7-alpine

WORKDIR /code

ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

COPY requirements.txt requirements.txt
COPY templates/ templates/
COPY app.py app.py

RUN apk add --no-cache gcc musl-dev linux-headers
RUN pip install -r requirements.txt

EXPOSE 5000

CMD ["flask", "run"]