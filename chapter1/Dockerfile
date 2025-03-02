# Alpine 3.21 ベースの golang 1.24.0 のイメージをベースとして使用
FROM golang:1.24.0-alpine3.21

LABEL maintainer="Tatsuro Miyazaki <tatsumiya05@gmail.com>"

# ビルドを行うマシン上の main.go ファイルをコンテナにコピー
COPY ./main.go ./

# ビルド時にコンテナ内でコマンドを実行
RUN go build -o ./go-app ./main.go

# 実行ユーザを指定
USER nobody

# コンテナ起動時に実行するコマンドを定義
ENTRYPOINT ["./go-app"]
