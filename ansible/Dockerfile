# Install Ansible into the standard Alpine image
# Set it to run as UID 1000
FROM alpine:latest
RUN apk add ansible aws-cli openssh-client && \
    addgroup -g 1000 group && \
    adduser -G group -u 1000 -h /home/user -D user && \
    mkdir /shared && \
    chown user:group /shared
USER 1000:1000
