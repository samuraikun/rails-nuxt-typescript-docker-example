FROM node:15.5.0-alpine
RUN apk update && apk upgrade && \
    apk add --no-cache bash git openssh \
    npm i -g yarn
RUN mkdir -p /myapp/frontend
WORKDIR /myapp/frontend
COPY package.json /myapp/frontend/package.json
# COPY yarn.lock /myapp/frontend/yarn.lock
RUN yarn install
