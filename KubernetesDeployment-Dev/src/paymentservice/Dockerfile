
FROM node:14-alpine

WORKDIR /usr/src/app

COPY package*.json ./
COPY . /app

RUN npm install

EXPOSE 4051

CMD [ "npm", "start" ]