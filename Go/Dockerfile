# Start from the official Golang image
FROM golang:1.15

# Set the working directory
WORKDIR /app

# Copy the Go files
COPY . .

# Build the application
RUN go build -o myapp-go .

# Run the binary
CMD ["./myapp-go"]
