FROM node:lts-alpine3.17

ENV CI=true
ENV PORT=3000

WORKDIR /code
COPY package.json /code/package.json
COPY package-lock.json /code/package-lock.json
RUN npm install
# carrying out unit test
RUN npm test -v
COPY . /code
# carrying out unit test

CMD ["npm", "start"]