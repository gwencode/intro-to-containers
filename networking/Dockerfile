FROM node:12-stretch

USER node

WORKDIR /home/node/code

COPY --chown=node:node package-lock.json package.json ./

RUN npm install

COPY --chown=node:node . .

CMD [ "node", "index.js" ]
