# syntax=docker/dockerfile:1

FROM node:latest
ENV NODE_ENV=production

WORKDIR /app

COPY ["package.json", "package-lock.json", "./"]

RUN npm config set registry https://nexus.eurocontrol.int/repository/npmjs-public/

RUN npm config set _auth=cDJvM2VJTVA6YkFUbzFyWDF3MnJQcWtaamRRVDBmRVk3aVRQd19UczdJeFUyMWljVXdjSW4=

RUN npm install --production 

COPY . .

EXPOSE 8080
CMD [ "node", "server.js" ]
