FROM debian:bullseye-slim

ENV STEAMCMD_ROOT /root/steamcmd
RUN apt update && apt install -y lib32gcc-s1 curl && \
    mkdir -p ${STEAMCMD_ROOT} && cd ${STEAMCMD_ROOT} && \
    curl -o steamcmd_linux.tar.gz "https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz" && \
    tar zxf steamcmd_linux.tar.gz && \
    rm steamcmd_linux.tar.gz && \
    apt remove -y curl && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*
