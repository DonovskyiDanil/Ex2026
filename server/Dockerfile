ARG VERSION=lts-alpine

FROM node:$VERSION

ARG NODE_ENV="development"

RUN mkdir -p /server/public/images

WORKDIR /server

COPY package*.json ./

RUN npm install

RUN chown -R node:node /server/node_modules

COPY . .

EXPOSE 3000

CMD ["npm", "start"]