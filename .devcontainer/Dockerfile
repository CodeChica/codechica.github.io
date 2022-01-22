FROM mcr.microsoft.com/vscode/devcontainers/go:0-1
ENV LANG=en_US.UTF-8
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update -y && apt-get install -y --no-install-recommends ruby-dev
RUN gem install bundler -v "~>2.0"
