FROM node:21 AS base

WORKDIR /app
COPY package.json ./
RUN npm install
COPY . ./

FROM node:21-slim AS run
WORKDIR /app
COPY --from=base /app ./

EXPOSE 3000

CMD ["node", "app.js"]
