#ARG DEBIAN_FRONTEND=noninteractive
#ARG VARIANT=bullseye
#FROM mcr.microsoft.com/vscode/devcontainers/base:${VARIANT}

FROM ubuntu:22.04

#git is required in codespaces_local.sh git clone dotfiles repo
RUN apt update && apt install git jq netcat -y

RUN useradd -ms /bin/bash vscode
# To create an user without a password, use passwd -d 
RUN passwd -d vscode
# RUN ln -s /home /Users
