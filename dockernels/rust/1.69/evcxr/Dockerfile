FROM rust:1.69.0-slim-bullseye

COPY config/mirrors/cn/cargo_config /.cargo/config
COPY config/mirrors/cn/debian_bullseye_config /etc/apt/sources.list

RUN rm -Rf /var/lib/apt/lists/* && \
  apt-get update  && \
  apt-get install -y \
  pkg-config \
  libssl-dev \
  apt-transport-https \
  ca-certificates \
  build-essential \
  cmake

# RUN rustup component add rust-src
RUN cargo install evcxr_jupyter
CMD evcxr_jupyter --control_file $DOCKERNEL_CONNECTION_FILE