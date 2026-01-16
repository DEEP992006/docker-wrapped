FROM node:20.20.0-alpine3.23

RUN npm i -g pnpm && npm --version

WORKDIR /home
COPY package*.json .

RUN pnpm i

COPY index.js index.js

EXPOSE 8000

CMD ["npm","start"]