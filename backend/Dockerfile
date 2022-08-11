FROM golang:1.18

WORKDIR /app

COPY go.mod ./
COPY go.sum ./
RUN go mod download
RUN go mod download github.com/gomodule/redigo

COPY *.go ./
 
RUN go build -o /docker-gs-ping

EXPOSE 8080
CMD [ "/docker-gs-ping" ]

