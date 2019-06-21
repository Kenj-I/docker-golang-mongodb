FROM golang:1.12-alpine

ENV TZ=Asia/Tokyo
RUN apk add --update --no-cache tzdata && \
  cp /usr/share/zoneinfo/${TZ} /etc/localtime && \
  echo ${TZ} > /etc/timezone

# golangをwatchしてビルドしてくれるライブラリ
RUN apk add --update --no-cache git && \
  go get github.com/oxequa/realize