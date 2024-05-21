FROM debian:bookworm-slim

# update and curl
RUN apt update
RUN apt install -y curl

# fs
WORKDIR /usr/src
COPY . .

# node
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
RUN apt install -y nodejs

# program
RUN npm install
RUN npm run build
RUN npm install -g serve

ENTRYPOINT ["serve", "-s", "-l", "5000", "build"]
