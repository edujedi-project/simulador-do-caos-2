FROM node:20.9.0
WORKDIR /app
COPY package*.json ./
RUN npm install express acme-http-01-koa
RUN apt update && apt install stress --yes
COPY . .
RUN npm run compile
EXPOSE 3000
CMD ["npm", "start"]
