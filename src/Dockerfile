FROM node:20.9.0-alpine3.18
ARG NODE_MAJOR=20
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]
