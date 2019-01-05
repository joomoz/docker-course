FROM ubuntu:16.04 

ENV FRONT_URL=http://localhost:5000
EXPOSE 8000
WORKDIR /backend

RUN apt-get update && apt-get install -y \
    curl git && \
    git clone https://github.com/docker-hy/backend-example-docker.git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/* && \
    npm install

CMD npm start