# Use the official Node.js image from Docker Hub
FROM node:lts-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the server code to the container
COPY . .

# Expose the port the server will run on
EXPOSE 5000

# Start the server
CMD ["npm", "start"]
