FROM node:16.5.0

RUN mkdir -p /app/node_modules && chown -R node:node /app
WORKDIR /app
COPY package*.json ./

USER node
RUN npm install --production
COPY --chown=node:node . .

EXPOSE 8080

CMD ["node", "server.js"]