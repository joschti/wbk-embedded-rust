FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

# install some basics
RUN apt-get update && apt-get -y upgrade
RUN apt-get -y install \
    git \
    curl

# switch to non-root user
USER vscode

# sets the working directory for any RUN, CMD, ENTRYPOINT, COPY and ADD instructions that follow
WORKDIR /home/vscode

# install Rust
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs -o install_rust.sh \
    && sh install_rust.sh -y \
    && rm install_rust.sh
    