ARG BUILD_ARCH
FROM ghcr.io/home-assistant/${BUILD_ARCH}-base:latest

# Install Go
RUN apk add --no-cache go git

# Set Go environment variables
ENV GO111MODULE=on

# Copy and build the Go application
WORKDIR /app
COPY sma_battery_controller.go go.mod go.sum /app/
RUN go build -o /sma_battery_controller

# Copy the run script
COPY run.sh /
RUN chmod +x /run.sh

CMD [ "/run.sh" ]