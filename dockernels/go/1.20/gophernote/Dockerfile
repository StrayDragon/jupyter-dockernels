FROM golang:1.20.2-bullseye

COPY config/mirrors/cn/debian_bullseye_config /etc/apt/sources.list

RUN go env -w GO111MODULE=on
RUN go env -w GOPROXY=https://goproxy.cn,direct
RUN go install github.com/gopherdata/gophernotes@v0.7.5

CMD gophernotes $DOCKERNEL_CONNECTION_FILE

