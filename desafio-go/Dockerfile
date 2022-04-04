FROM golang:1.18-alpine as builder

WORKDIR /usr/app

COPY ./src .

RUN go mod init desafio-go && \
    go build

FROM scratch

WORKDIR /usr/app

COPY --from=builder /usr/app/desafio-go .

CMD ["/usr/desafio-go"]
