FROM python:3.12.4-alpine3.20

LABEL maintainer="Cristian Tangarife <cgt9145@gmail.com>"

RUN apk update
RUN apk upgrade
RUN apk add --no-cache bash git openssh vim 
RUN apk add --no-cache python3-dev libstdc++ 
RUN apk add --no-cache g++
RUN apk add --no-cache postgresql-dev gcc python3-dev musl-dev 
RUN ln -s /usr/include/locale.h /usr/include/xlocale.h


WORKDIR /var/www/

## -------------------------------------------
## Create Volumen for data local
## -------------------------------------------
ADD ./build/flask/requirements.txt /var/www/pre/requirements.txt

WORKDIR /var/www/pre

RUN pip install --upgrade pip

RUN pip install -r requirements.txt

# Añadir el comando para descargar el modelo de SpaCy
RUN python -m spacy download en_core_web_sm

WORKDIR /var/www/

RUN rm -rf pre

WORKDIR /var/www/encuesta-validator