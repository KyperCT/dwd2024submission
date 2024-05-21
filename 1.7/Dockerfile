# Start from the alpine image
FROM ubuntu:22.04

COPY script.sh .

RUN apt update
RUN apt install -y curl
RUN chmod +x ./script.sh
CMD ./script.sh
