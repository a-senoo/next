FROM node:20.14.0-alpine

WORKDIR /frontend

# 依存関係のインストール
COPY ./frontend/package.json ./frontend/yarn.lock ./
RUN yarn install

# アプリケーションのファイルをコピー
COPY . .

# プロダクションビルドの実行
RUN yarn build

# アプリケーションを起動
CMD ["yarn", "start"]