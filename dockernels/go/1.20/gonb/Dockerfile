FROM golang:1.20.2-bullseye

COPY config/mirrors/cn/debian_bullseye_config /etc/apt/sources.list

RUN go env -w GO111MODULE=on
RUN go env -w GOPROXY=https://goproxy.cn,direct
RUN go install github.com/janpfeifer/gonb@latest && \
    go install golang.org/x/tools/cmd/goimports@latest && \
    go install golang.org/x/tools/gopls@latest

CMD gonb --kernel $DOCKERNEL_CONNECTION_FILE

