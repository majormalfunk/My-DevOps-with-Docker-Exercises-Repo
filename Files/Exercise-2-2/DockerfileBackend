FROM ubuntu:16.04 

WORKDIR /exercise
EXPOSE 8000

RUN apt-get update && apt-get install -y curl && apt-get install -y git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN git clone https://github.com/docker-hy/backend-example-docker.git /exercise
RUN touch logs.txt
RUN npm install
CMD npm start

