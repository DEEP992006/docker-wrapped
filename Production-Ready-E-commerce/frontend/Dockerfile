FROM node:20.20.0-alpine3.22

WORKDIR /app

# Copy package files first for better caching
COPY package.json pnpm-lock.yaml .

# Install pnpm and dependencies
RUN npm install -g pnpm && pnpm install

# Copy config files
COPY tsconfig.json next.config.ts postcss.config.mjs components.json eslint.config.mjs .

# Copy source code folders
COPY app app
COPY components components
COPY lib lib
COPY public public

EXPOSE 3000

CMD ["pnpm", "dev"]
