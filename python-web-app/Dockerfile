#### Stage 1 ###
# Build virtualenv in apline image 

FROM alpine AS build

# Name and email of the person who maintains the file
MAINTAINER Deepak Verma  deepcloud.28@gmail.com

RUN apk add python3 
RUN python3 -m venv /venvflask &&  /venvflask/bin/pip install --upgrade pip && source /venvflask/bin/activate
COPY ./app-source-code/requirements.txt /requirements.txt
RUN /venvflask/bin/pip3 install --disable-pip-version-check -r /requirements.txt

### Stage 2 ###
#Change file owner  and copy the virtualenv into a distroless image

FROM gcr.io/distroless/python3
COPY --from=build --chown=nonroot:nonroot /venv /venv
COPY ./app-source-code/ /venv 
WORKDIR /venv 
EXPOSE 5000
USER nonroot
ENTRYPOINT ["/venvflask/bin/python3","-m" , "flask", "run", "--host=0.0.0.0"]
