FROM node:12-alpine

WORKDIR /code

COPY package.json package-lock.json /code/

RUN npm install chalk

COPY . /code/

EXPOSE 3000

#RUN node ./scripts/start.js
CMD ["node", "./scripts/start.js"]