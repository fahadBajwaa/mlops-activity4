# Use Node.js LTS version
FROM node:16-alpine

# Set working directory in the container
WORKDIR /app

# Copy package.json and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of your application
COPY . .

# Expose port 3000 for the frontend app
EXPOSE 3000

# Start the frontend
CMD ["npm", "start"]
