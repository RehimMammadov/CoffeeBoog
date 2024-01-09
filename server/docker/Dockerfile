# Use an official Node.js runtime as a base image
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and yarn.lock to the working directory
COPY package*.json yarn.lock ./

# Install application dependencies using yarn
RUN yarn install --production

# Copy the rest of the application code to the working directory
COPY . .

# Expose the port that your Nest.js application will run on
EXPOSE 3000

# Command to run your Nest.js application
CMD ["yarn", "start:prod"]
