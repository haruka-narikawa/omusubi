FROM node:latest

WORKDIR /usr/src/front

COPY ./package*.json .

RUN npm install

COPY . .

COPY .env.production.local .env

RUN npm run build

# ポートを公開
# EXPOSE 80

# コンテナ起動時に実行するコマンドを指定
CMD ["npm", "run", "start:server"]