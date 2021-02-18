FROM node:15-buster-slim

WORKDIR /frontend

ADD package.json yarn.lock ./
RUN yarn install && yarn cache clean --all
ADD . .
RUN yarn build

ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/frontend/node_modules/.bin
EXPOSE 5000/tcp

CMD ["serve" ,"-s", "build" ,"-l", "3000"]
