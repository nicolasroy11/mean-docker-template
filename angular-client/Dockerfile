# Create image based on the official Node 6 image from dockerhub
FROM node:6

# Create a directory where our app will be placed
# RUN is the command you use to run terminal commands. the -p: Create parent directories 
# as necessary. When this option is specified, no error is reported if a directory already exists.
RUN mkdir -p /usr/src/app

# Change directory so that our commands run inside this new directory. WORKDIR = cd.
# If we don't set this, the default is /
WORKDIR /usr/src/app

# Copy dependency definitions. COPY <src> <dest> src is with respect to the Dockerfile, dest is
# the destination inside the docker container file system
COPY package.json /usr/src/app

# Install dependecies
RUN npm install

# Get all the code needed to run the app
COPY . /usr/src/app

# Expose the port the app runs in
EXPOSE 4200

# Serve the app
CMD ["npm", "start"]