# Use an official Node.js runtime as the base image
FROM node:14

# Set the working directory in the container to /app
WORKDIR /frontend-ep

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install the application dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Build the app for production
RUN yarn build

# Use an official Nginx runtime as the base image for the production build
FROM nginx:1.19-alpine

# Copy the build output to replace the default Nginx contents.
COPY --from=0 /frontend-ep/build /usr/share/nginx/html

# Expose port 80
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]