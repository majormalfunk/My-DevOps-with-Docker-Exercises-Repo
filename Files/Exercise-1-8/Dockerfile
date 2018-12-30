FROM ubuntu:16.04 

WORKDIR /exercise
EXPOSE 8080

RUN apt-get update && apt-get install -y curl && apt-get install -y wget default-jdk
RUN wget https://github.com/majormalfunk/ohtutips/releases/download/release/ohtutips.jar
CMD java -jar ohtutips.jar
