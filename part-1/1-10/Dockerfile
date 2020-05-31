# The base image.
FROM ubuntu:16.04

# Set the working directory.
WORKDIR /usr/src/app

# Run the command inside your image filesystem.
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN npm install
RUN npm install -g serve
RUN serve -s -l 5000 dist

# Inform Docker that the container is listening on the specified port at runtime.
EXPOSE 5000

# Run the specified command within the container.
CMD [ "npm start" ]
