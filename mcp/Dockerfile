FROM node:20-slim
RUN corepack enable && corepack prepare pnpm@9 --activate
WORKDIR /app
COPY package.json pnpm-lock.yaml ./
RUN pnpm install --frozen-lockfile --prod
COPY server.js ./
ENV NODE_ENV=production
CMD ["node", "server.js"]
