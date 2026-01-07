FROM oven/bun:1.1.29

WORKDIR /app

COPY package.json bun.lock ./
RUN bun install --frozen-lockfile

COPY . .

ENV NODE_ENV=production
EXPOSE 3000

CMD ["sh", "-c", "bunx prisma generate && bun run src/server.ts"]