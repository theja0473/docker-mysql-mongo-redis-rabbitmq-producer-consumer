FROM nikolaik/python-nodejs

ADD requirements.txt /tmp/requirements.txt
RUN pip install -U -r /tmp/requirements.txt

USER pn

WORKDIR /home/pn/app
VOLUME /home/pn/app
EXPOSE 5000
