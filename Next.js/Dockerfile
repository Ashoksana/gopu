# Base image
FROM node:14-alpine
# Set working directory
WORKDIR /app
# Install dependencies
COPY package.json package-lock.json ./
RUN npm install
# Copy source files
COPY . .
# Build the application
RUN npm run build
# Start the application
CMD ["npm", "start"]
