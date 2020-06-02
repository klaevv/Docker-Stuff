# The base image.
FROM ubuntu:16.04

WORKDIR /frontend-example-docker

ENV API_URL="http://localhost:8000"

# Run the command inside your image filesystem.
RUN apt-get update && apt-get install -y curl && apt-get install -y git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

RUN git clone https://github.com/docker-hy/frontend-example-docker

RUN npm install
RUN npm install -g serve

# Inform Docker that the container is listening on the specified port at runtime.
EXPOSE 5000

# Run the specified command within the container.
CMD npm start
