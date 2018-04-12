FROM golang:1.8
RUN go get -d github.com/alexbadm/wex-exchange-rate
WORKDIR /go/src/github.com/alexbadm/wex-exchange-rate
RUN mkdir /build
RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o /build/app .

FROM alpine:latest
RUN apk --no-cache add ca-certificates
WORKDIR /root/
COPY --from=0 /build/app .
CMD ["./app"]
