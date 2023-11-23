FROM node:lts-alpine

WORKDIR /app

COPY package.json .

RUN yarn install

COPY . .

RUN yarn run build

EXPOSE 3000

RUN yarn global add serve

CMD [ "serve", "-s","build" ]