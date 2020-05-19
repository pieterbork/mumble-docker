FROM rust:1.39 

RUN apt-get update && apt-get install libnice-dev clang -y
RUN git clone https://github.com/johni0702/mumble-web-proxy
WORKDIR mumble-web-proxy
RUN cargo build --release

RUN cp target/release/mumble-web-proxy /bin/

COPY entrypoint.sh /
CMD ["/entrypoint.sh"]
