# Use an official Node.js runtime as the base image
FROM node:14
# Set the working directory in the container to /app
WORKDIR /backend-ep
# Copy package.json and package-lock.json to the working directory
COPY package*.json ./
# Install the application dependencies
RUN npm install
# Copy the rest of the application code to the working directory
COPY . .
# Expose port 3000
EXPOSE 3000
# Start the application
CMD ["npm", "start"]