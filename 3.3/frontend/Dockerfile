FROM ubuntu:16.04 

ENV API_URL=http://localhost:8000
EXPOSE 5000
WORKDIR /frontend

RUN apt-get update && apt-get install -y \
    curl git && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/* && \
    npm install && \
    useradd -m app

USER app

CMD npm start