FROM golang:alpine AS builder

WORKDIR /app

COPY . .

RUN go build -o /go/bin/hello

FROM scratch

COPY --from=builder /go/bin/hello /go/bin/hello

ENTRYPOINT ["/go/bin/hello"]