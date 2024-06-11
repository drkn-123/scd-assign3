# Use an official Node.js runtime as the base image
FROM node:14
# Set the working directory in the container to /backend-ep
WORKDIR /backend-ep
# Copy package.json and package-lock.json to the working directory
COPY package*.json ./
# Install the application dependencies
RUN npm install
# Copy the rest of the application code to the working directory
COPY . .
# Expose port 3000 for the backend server
EXPOSE 3000
# Start the backend server
CMD ["npm", "start"]