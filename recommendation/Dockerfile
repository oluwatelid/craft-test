# syntax=docker/dockerfile:1

FROM golang:1.19

# Set destination for COPY
WORKDIR /recommendation

# Download Go modules
COPY . ./
RUN go mod download

RUN go build -o ./app

EXPOSE 8080

# Run
CMD ["./app"]
