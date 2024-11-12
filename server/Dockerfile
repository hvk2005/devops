# Use an official Node.js runtime as a parent image
FROM node:16

# Set the working directory in the container
WORKDIR /app

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install backend dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Expose the backend port (usually 5000)
EXPOSE 5000

# Start the backend server
CMD ["npm", "start"]
