FROM python:3.8
MAINTAINER Vladimir Alchin 'vladimiralchin@ya.ru'
RUN apt-get update -y && apt-get install -y

RUN apt install -y build-essential
RUN apt-get install curl

COPY . /app
WORKDIR /app/

RUN pip install -r requirements.txt
EXPOSE 5000
ENTRYPOINT python app.py
