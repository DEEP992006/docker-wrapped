FROM node:20.20.0-alpine3.23

WORKDIR /home

COPY package*.json .
COPY tsconfig*.json .
COPY src/ src/
RUN npm i
RUN npm run build
EXPOSE 8000
CMD ["npm","start"]

