# The base image.
FROM ubuntu:16.04

# Set the working directory.
WORKDIR /backend-example-docker

# Run the command inside your image filesystem.
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs && npm install

COPY . .

RUN npm install

ENTRYPOINT npm start
