FROM golang AS gohello
WORKDIR /go/src
COPY ./src/hello.go .
RUN go build hello.go

FROM scratch
COPY --from=gohello /go/src/hello /
CMD ["/hello"]
