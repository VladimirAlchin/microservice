FROM ubuntu:20.04
MAINTAINER vladimir alchin "alchinvovka@gmail.com"
RUN apt-get update -y

# apt-get and system utilities
RUN apt-get update && apt-get install -y
RUN apt-get install curl -y
RUN apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release -y \
RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
RUN echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null \



COPY . /app
WORKDIR /app
