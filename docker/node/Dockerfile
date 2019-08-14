FROM node:10.15.0-alpine

RUN apk add npm && npm i -g http-server && apk add --no-cache bash

VOLUME /app

WORKDIR /app

EXPOSE 3000

CMD http-server

