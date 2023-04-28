FROM rust:1.69.0-slim-bullseye

COPY config/mirrors/cn/cargo_config /.cargo/config
COPY config/mirrors/cn/debian_bullseye_config /etc/apt/sources.list
COPY config/mirrors/cn/pypi_config /etc/pip.conf

RUN rm -Rf /var/lib/apt/lists/* && \
  apt-get update  && \
  apt-get install -y \
  pkg-config \
  libssl-dev \
  apt-transport-https \
  ca-certificates \
  build-essential \
  cmake \
  git \
  python3 python3-pip

WORKDIR /opt

RUN python3 -m pip install irust_kernel
RUN mkdir -p /root/.local/share/jupyter/kernels/irust
RUN git clone --depth 1 https://gitclone.com/github.com/sigmasd/irust && \
    cd irust && \
    cargo b --release --example re && \
    cp target/release/examples/re /root/.local/share/jupyter/kernels/irust

CMD python3 -m irust_kernel -f $DOCKERNEL_CONNECTION_FILE

