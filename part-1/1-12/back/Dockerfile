# The base image.
FROM ubuntu:16.04

# Set the working directory.
WORKDIR /backend-example-docker

ENV FRONT_URL="http://localhost:5000"

# Run the command inside your image filesystem.
RUN apt-get update && apt-get install -y curl && apt-get install -y git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs && npm install
RUN git clone https://github.com/docker-hy/backend-example-docker

RUN npm install

EXPOSE 8000

CMD npm start
