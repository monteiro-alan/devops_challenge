FROM node:16.13-bullseye-slim AS development
WORKDIR /usr/src/app
ENV NODE_ENV=development
COPY . .
RUN npm ci
CMD [ "npm", "run", "dev:watch" ]

FROM node:16.13-bullseye-slim AS staging
WORKDIR /usr/src/app
ENV NODE_ENV=staging
COPY . .
RUN npm ci --production
CMD [ "npm", "start" ]

FROM node:16.13-bullseye-slim AS production
WORKDIR /usr/src/app
ENV NODE_ENV=production
COPY . .
RUN npm ci --production
CMD [ "npm", "start" ]