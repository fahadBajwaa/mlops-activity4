# Use the Node.js LTS (Long Term Support) version as the base image
FROM node:16-alpine

# Set the working directory inside the Docker container
WORKDIR /app

# Copy package.json and package-lock.json (if available) to install dependencies
COPY package*.json ./

# Install all dependencies (including dev dependencies)
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Expose port 5000 to allow external access to the backend service
EXPOSE 5010

# Install nodemon globally to enable live-reloading during development
RUN npm install -g nodemon

# Start the application with nodemon for development mode (watch mode)
CMD ["nodemon", "server.js"]
