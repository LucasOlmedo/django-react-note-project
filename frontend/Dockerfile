# Use an official Node runtime as a parent image
FROM node:18

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json first to leverage Docker cache
COPY package*.json ./

# Install project dependencies
RUN npm install

# Copy the current directory contents into the container
COPY . .

# Make port 3000 available to the world outside this container
EXPOSE 3000

CMD ["npm", "run", "dev"]
