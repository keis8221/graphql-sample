# goバージョン
FROM golang:1.21.6-alpine

# アップデートとgit、alpine-sdkのインストール
RUN apk update && apk add git && apk add alpine-sdk

# 環境変数の設定
ENV APP_ROOT /app

# ディレクトリの作成
RUN mkdir $APP_ROOT

# ワーキングディレクトリの設定
WORKDIR $APP_ROOT

# Goの詳細設定
ENV CGO_ENABLED=1 \
  GOOS=linux \
  GOARCH=amd64 \
  GO111MODULE=on

# ルートディレクトリを作業ディレクトリにコピー
COPY . $APP_ROOT


