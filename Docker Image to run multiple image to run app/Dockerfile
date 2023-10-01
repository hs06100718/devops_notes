FROM python:3 AS base

RUN apt-get -y update

FROM base AS requirements

COPY app.py requirements.txt code/

WORKDIR /code

RUN pip3 install -r requirements.txt

FROM requirements as test

CMD ["python3", "app.py"]