# Use the official Node.js image from Docker Hub
FROM node:lts-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the React code to the container
COPY . .

# Build the React app
RUN npm run build

# Install a lightweight HTTP server to serve the built app
RUN npm install -g serve

# Expose the port that the React app will run on
EXPOSE 3000

# Start the server
CMD ["serve", "-s", "build"]
