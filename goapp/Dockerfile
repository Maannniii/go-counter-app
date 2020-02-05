# Build ENV
FROM golang:alpine AS build
COPY ./src /src
WORKDIR /src
RUN apk --no-cache add make && make build

# Deployment env
FROM alpine
WORKDIR /app
ENV DEMO_APP_ADDR :80
ENV DEMO_REDIS_ADDR localhost:6379
COPY --from=build /src/demo.bin /app/
ENTRYPOINT ./demo.bin
