FROM node:15-buster-slim

WORKDIR /backend

ADD package.json yarn.lock ./
RUN yarn install && \
    yarn cache clean --all
ADD . .

EXPOSE 8000/tcp

CMD ["node" ,"index.js"]
