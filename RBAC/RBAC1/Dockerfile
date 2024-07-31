FROM alpine:latest

RUN apk add --no-cache bash curl

RUN curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" && \
    install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

COPY ./script.sh  .

RUN chmod +x ./script.sh

ENTRYPOINT ["./script.sh"]
