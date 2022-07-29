FROM node:18.6.0-alpine

ENV APP_HOME /live-chat-vuejs
RUN mkdir -p $APP_HOME
WORKDIR $APP_HOME

RUN apk update && npm install -g @vue/cli
COPY $APP_HOME/package.json $APP_HOME/package.json
RUN npm install