# Start from the Node.js image
FROM node:14

# Set the working directory
WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy the Next.js files
COPY . .

# Build the application
RUN npm run build

# Start the application
CMD ["npm", "start"]
