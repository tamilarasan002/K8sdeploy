FROM golang:1.16.4-alpine

WORKDIR /src

COPY go.mod go.sum ./

RUN go mod download

COPY . .

RUN go build -o productcatalogservice .

COPY --from=builder /productcatalogservice ./server
COPY products.json .

EXPOSE 3550

ENV NAME Productcatalogservice

CMD [ "./productcatalogservice" ]
