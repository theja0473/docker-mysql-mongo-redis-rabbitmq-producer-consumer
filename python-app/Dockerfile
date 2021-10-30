FROM python:3.7

ADD requirements.txt /tmp/requirements.txt
RUN pip install -U -r /tmp/requirements.txt

ADD . /app
WORKDIR /app
VOLUME /app
EXPOSE 5000
