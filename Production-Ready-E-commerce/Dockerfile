FROM node:20.20.0-alpine3.22
WORKDIR /home
COPY db/ db/
COPY routes/ routes/
COPY app.js .
COPY drizzle.config.js .
COPY index.js .
COPY package.json .
COPY pnpm-lock.yaml .
RUN npm --version
RUN npm i -g pnpm
RUN pnpm i
CMD ["sh", "-c", "npx drizzle-kit push && node app.js"]

