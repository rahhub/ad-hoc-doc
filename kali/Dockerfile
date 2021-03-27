# Bundle some useful tools into the standard Kali image
FROM kalilinux/kali:latest
RUN apt-get update && \
    apt-get install -y iproute2 nmap procps sslscan && \
    apt-get clean
    