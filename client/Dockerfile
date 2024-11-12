# Use an official Node.js runtime as a parent image
FROM node:16

# Set the working directory in the container
WORKDIR /app

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install frontend dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Build the frontend app for production
RUN npm run build

# Install serve to serve the production build
RUN npm install -g serve

# Expose the frontend port (usually 3000)
EXPOSE 3000

# Start the frontend server
CMD ["serve", "-s", "build"]
