FROM golang:1.17 as build_img
COPY main.go .
RUN go build -o /app main.go

From ubuntu:18.04
COPY --from=build_img /app .
ENTRYPOINT ["./app"]
