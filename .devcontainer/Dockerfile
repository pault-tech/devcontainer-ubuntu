# ARG DEBIAN_FRONTEND=noninteractive
#ARG VARIANT=bullseye
#FROM mcr.microsoft.com/vscode/devcontainers/base:${VARIANT}

FROM ubuntu:22.04

#git is required in codespaces_local.sh git clone dotfiles repo
RUN apt update && apt -y install \
git \
jq \
netcat \
curl \
ca-certificates \
less \
software-properties-common \
iputils-ping \
ssh \
gnupg \
screen \
sudo \
vim \
python3-pip \
rsync

#emacs 29
RUN add-apt-repository ppa:ubuntuhandbook1/emacs
RUN DEBIAN_FRONTEND=noninteractive apt -y install emacs-nox

RUN useradd -G sudo -ms /bin/bash vscode
# To create an user without a password, use passwd -d 
RUN passwd -d vscode
# RUN ln -s /home /Users

