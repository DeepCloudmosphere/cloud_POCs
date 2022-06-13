
				### Dockerfile 56 ###

#### Stage 1 ###
# Build virtualenv in apline image 

FROM alpine AS FLASK

# Name and email of the person who maintains the file
MAINTAINER Deepak Verma  deepcloud.28@gmail.com

RUN apk add python3 
RUN python3 -m venv /venv &&  /venv/bin/pip install --upgrade pip && source /venv/bin/activate
COPY app-source-code/requirements.txt /requirements.txt
RUN /venv/bin/pip3 install --disable-pip-version-check -r /requirements.txt
COPY app-source-code/app.py /venv/
WORKDIR /venv/ 
ENTRYPOINT ["/venv/bin/python3", "app.py"]
