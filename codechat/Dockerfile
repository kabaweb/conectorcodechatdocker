FROM node:16.19.0

LABEL version="2.0.0" description="Api to control whatsapp features through http requests." 
LABEL maintainer="Cleber Wilson" git="https://github.com/jrCleber"
LABEL contact="contato@codechat.dev"

RUN apt-get update -y
RUN apt-get upgrade -y

WORKDIR /home/api

COPY ./package.json .

# see https://github.com/code-chat-br/whatsapp-api/blob/main/Docker/dev.env

# Set "true" to dynamically insert environment variables as described in the "./dev.env" file


RUN npm i

COPY . .

EXPOSE 8080

RUN npm run build

CMD [ "node", "./dist/src/main.js" ]
