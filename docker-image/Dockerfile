FROM alpine:3.7

# Install Docker client
ARG DOCKER_VERSION=1.12.6

COPY clean-image.sh  /usr/local/bin/

RUN apk add --update --no-cache \
                      curl \
                      tar && \
    curl -fsSL https://get.docker.com/builds/Linux/x86_64/docker-$DOCKER_VERSION.tgz | tar --strip-components=1 -xz -C /usr/local/bin docker/docker

RUN chmod +x /usr/local/bin/clean-image.sh

ENTRYPOINT ["/usr/local/bin/clean-image.sh"]
