FROM ruby:3.2-slim

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    git \
    build-essential \
    libffi-dev \
    libyaml-dev \
    zlib1g-dev && \
    rm -rf /var/lib/apt/lists/*

RUN gem install jekyll bundler
