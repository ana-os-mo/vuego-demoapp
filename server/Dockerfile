FROM golang:1.17.3-alpine3.14

WORKDIR /app

COPY go.mod .
COPY go.sum .
RUN go mod download

COPY *.go .
RUN go build -o backend-img .

EXPOSE 4000

CMD [ "/app/backend-img" ]