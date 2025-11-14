FROM golang:1.20 AS build

WORKDIR /app
COPY go.mod go.sum ./

COPY . ./
RUN go build -o app

FROM golang:1.20 AS run
WORKDIR /app

COPY --from=build app ./

EXPOSE 8080

CMD ["./app"]
