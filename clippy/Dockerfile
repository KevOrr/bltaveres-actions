FROM rust:slim

LABEL "com.github.actions.name"="clippy"
LABEL "com.github.actions.description"="Provides linting and fixes for Rust using clippy"
LABEL "com.github.actions.icon"="user-check"
LABEL "com.github.actions.color"="purple"

LABEL "repository"="http://github.com/bltavares/actions"
LABEL "homepage"="http://github.com/bltavares/actions"
LABEL "maintainer"="Bruno Tavares <connect+githubactions@bltavares.com>"

RUN rustup component add clippy && cargo install cargo-fix

RUN apt-get update -qq && apt-get install -qqy --no-install-recommends curl jq bash git libssl-dev zlib1g-dev pkg-config \
  && rm -rf /var/lib/apt/lists/*

COPY lib.sh /lib.sh
COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
