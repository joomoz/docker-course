FROM ubuntu:16.04 

WORKDIR /mydir 
RUN apt-get update && apt-get install -y curl  
COPY website.sh .
RUN chmod +x website.sh

CMD sh website.sh