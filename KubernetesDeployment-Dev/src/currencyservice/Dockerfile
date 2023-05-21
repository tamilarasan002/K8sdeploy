
FROM node:14-alpine

WORKDIR /app

COPY package*.json ./
COPY . /app

RUN npm install

EXPOSE  7000

CMD [ "npm", "start" ]