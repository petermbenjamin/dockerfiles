# docker run --rm \
#      -v $PWD:/hugo
#      hugo new site /hugo/foo

FROM debian:buster-slim
LABEL maintainer "Peter Benjamin <petermbenjamin@gmail.com>"
RUN apt-get update && apt-get install -y \
       ca-certificates \
       curl \
       --no-install-recommends \
       && rm -rf /var/lib/apt/lists/*
ENV HUGO_VERSION 0.53
RUN curl -sSL "https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_${HUGO_VERSION}_Linux-64bit.tar.gz" | tar -vxzC /usr/local/bin

ENTRYPOINT ["hugo"]

