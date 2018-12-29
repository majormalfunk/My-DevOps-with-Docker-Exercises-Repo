FROM ubuntu:16.04 

WORKDIR /exercise
RUN apt-get update && apt-get install -y curl

COPY curlscript.sh .
CMD chmod +x ./curlscript.sh
CMD ./curlscript.sh
