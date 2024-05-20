# Start from the official Golang image to create a build artifact.
FROM golang:1.16 as builder

# Set the working directory outside of GOPATH to enable the support for modules.
WORKDIR /app

# Copy the go.mod and go.sum files first to leverage Docker cache.
COPY go.mod go.sum ./

# Download the module dependencies.
RUN go mod download

# Copy the rest of the application source code.
COPY . .

# Build the application.
RUN CGO_ENABLED=0 GOOS=linux go build -o MyApp .

# Use a Docker multi-stage build to create a lean production image.
FROM alpine:latest

# Copy the compiled application from the builder stage.
COPY --from=builder /app/MyApp /MyApp

# Expose port 8080.
EXPOSE 8080

# Run the compiled binary.
CMD ["/MyApp"]
