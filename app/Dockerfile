# syntax=docker/dockerfile:1

FROM node:latest
ENV NODE_ENV=production

WORKDIR /app

COPY ["package.json", "package-lock.json", "./"]

RUN npm config set registry http://registry.npmjs.org/

RUN npm config set strict-ssl false

RUN npm install --production 

COPY . .

EXPOSE 8080
CMD [ "node", "server.js" ]
