FROM node:15-alpine

ENV NEXT_TELEMETRY_DEBUG=1

WORKDIR /myapp

RUN apk add --no-cache libtool autoconf automake build-base python3 git

COPY package.json yarn.lock /myapp/

RUN yarn install --frozen-lockfile

COPY ./ /myapp

EXPOSE 3000
