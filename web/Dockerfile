FROM node:16.11-bullseye-slim AS builder
WORKDIR /usr/src/app
COPY package.json ./

FROM builder AS dev
ENV NODE_ENV=development
RUN npm install

FROM builder AS prod
ENV NODE_ENV=production
RUN npm install

FROM node:16.11-bullseye-slim AS development
WORKDIR /usr/src/app
ENV NODE_ENV=development
COPY --from=dev /usr/src/app /usr/src/app
COPY . .
CMD [ "npm", "run", "dev:watch" ]

FROM node:16.11-bullseye-slim AS production
WORKDIR /usr/src/app
ENV NODE_ENV=production
COPY --from=prod /usr/src/app /usr/src/app
COPY . .
CMD [ "npm", "start" ]