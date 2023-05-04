FROM node:16.20.0

WORKDIR /home/node
RUN git clone https://github.com/w3nder/chatwoot-codechat.git /home/node/app

WORKDIR /home/node/app

COPY .env /home/node/app/

RUN npm install
RUN npm run build

WORKDIR /home/node/app

ENTRYPOINT ["node", "dist/app.js"]
