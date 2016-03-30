FROM ubuntu:latest

ENV CONFD_VERSION="0.11.0" \
    CONFD_URL="https://github.com/kelseyhightower/confd/releases/download"

RUN set -x \
	&& apt-get update && apt-get install -y wget --no-install-recommends && rm -rf /var/lib/apt/lists/* \
  && wget --no-check-certificate --retry-connrefused -t 5 ${CONFD_URL}/v${CONFD_VERSION}/confd-${CONFD_VERSION}-linux-amd64 -O /bin/confd \
  && chmod +x /bin/confd \
  && apt-get purge -y --auto-remove wget
