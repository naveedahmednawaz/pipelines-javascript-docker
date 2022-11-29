# syntax=docker/dockerfile:1

FROM node:latest
ENV NODE_ENV=production

WORKDIR /app

COPY ["package.json", "package-lock.json*", "./"]

RUN npm config set strict-ssl false

RUN npm install --production --omit=dev

COPY . .

EXPOSE 8080
CMD [ "node", "server.js" ]
