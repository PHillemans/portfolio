FROM node:12-alpine
WORKDIR /usr/src/app
COPY package*.json ./
run npm install
COPY . .
EXPOSE 1234
ENV HOST=0.0.0.0
CMD [ "npm", "start"]
