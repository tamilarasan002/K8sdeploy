FROM golang:1.16.4-alpine

WORKDIR /src

COPY go.mod go.sum ./

RUN go mod download

COPY . .

RUN go build -o shippingservice .

EXPOSE 50051

ENV NAME Shippingservice

CMD [ "./shippingservice" ]