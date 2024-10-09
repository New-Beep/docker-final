FROM golang:1.22.0-alpine

WORKDIR /app

COPY go.mod go.sum tracker.db *.go ./

RUN go mod download

RUN CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -o /my-app

CMD ["/my-app"]