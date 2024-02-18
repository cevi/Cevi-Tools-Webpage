FROM ruby:3.1-slim-bullseye as jekyll

# install prerequisites for Jeykell
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    zlib1g-dev \
    git \
    && rm -rf /var/lib/apt/lists/*
RUN gem install jekyll bundler

# workdir inside the container
WORKDIR /app

# install dependencies listed in Gemfile
COPY Gemfile /app/Gemfile
COPY Gemfile.lock /app/Gemfile.lock
RUN bundle config set --local path 'vendor/bundle'
RUN bundle install

COPY . /app

# launch the page in dev mode
CMD bundle exec jekyll serve --incremental --livereload --host 0.0.0.0 --port 4000