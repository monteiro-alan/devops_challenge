FROM node:16.11-bullseye-slim AS builder
WORKDIR /usr/src/app
COPY package.json ./
RUN npm install

FROM node:16.11-bullseye-slim AS intermediate
WORKDIR /usr/src/app
COPY --from=builder /usr/src/app /usr/src/app

FROM intermediate AS development
ENV env=development
COPY . .
CMD [ "npm", "run", "dev:watch" ]

FROM intermediate AS production
ENV env=production
COPY . .
CMD [ "npm", "start" ]