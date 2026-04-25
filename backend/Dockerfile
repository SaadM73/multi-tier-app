# Use official Node.js LTS image as base
FROM node:18-alpine
# Set working directory inside container
WORKDIR /app
# Copy package files first (for layer caching)
COPY package*.json ./
# Install dependencies
RUN npm install --production
# Copy the rest of the application code
COPY . .
# Expose the port the backend listens on
EXPOSE 3001
# Command to start the application
CMD ["node", "server.js"]
