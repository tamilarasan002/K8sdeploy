
FROM golang:1.16.4-alpine

WORKDIR /app

COPY go.mod go.sum ./

RUN go mod download

COPY . .

RUN go build -o checkoutservice .

EXPOSE 5050

ENV NAME Checkoutservice

CMD [ "./checkoutservice" ]
