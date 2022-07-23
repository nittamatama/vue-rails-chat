FROM node:18.6.0-alpine

ENV APP_HOME /live-chat-vuejs
RUN mkdir -p $APP_HOME
WORKDIR $APP_HOME

RUN apk update
COPY package.json .
RUN npm install