# Author: Anil Saravade
# Copyright: Copyright (©) 2020. SwapStyle. All rights reserved.

FROM python:2-alpine

WORKDIR /usr/src/app

COPY ./requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY ./app.py .