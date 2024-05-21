FROM debian:bookworm-slim

# update and golang
RUN apt update
RUN apt install -y golang-go curl

# fs
WORKDIR /usr/src
COPY . .

# build program
RUN go build


ENTRYPOINT ["./server"]
