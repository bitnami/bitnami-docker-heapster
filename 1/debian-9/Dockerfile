FROM bitnami/minideb:stretch as buildenv

RUN install_packages ca-certificates wget
RUN wget -nc -P /tmp/bitnami/pkg/cache/ https://downloads.bitnami.com/files/stacksmith/heapster-1.5.3-0-linux-amd64-debian-9.tar.gz && \
    echo "9650256120b78370a3196e15f72b9d7561a7c79c5148a2c185b7b2e6fc3296ff  /tmp/bitnami/pkg/cache/heapster-1.5.3-0-linux-amd64-debian-9.tar.gz" | sha256sum -c - && \
    tar -zxf /tmp/bitnami/pkg/cache/heapster-1.5.3-0-linux-amd64-debian-9.tar.gz -P --transform 's|^[^/]*/files|/opt/bitnami|' --wildcards '*/files' && \
    rm -rf /tmp/bitnami/pkg/cache/heapster-1.5.3-0-linux-amd64-debian-9.tar.gz

##################

FROM bitnami/minideb:stretch
LABEL maintainer "Bitnami <containers@bitnami.com>"

COPY --from=buildenv /opt/bitnami/heapster /opt/bitnami/heapster
ENV BITNAMI_APP_NAME="heapster" \
    BITNAMI_IMAGE_VERSION="1.5.3-debian-9-r11" \
    PATH="/opt/bitnami/heapster/bin:$PATH"

RUN install_packages ca-certificates

EXPOSE 8082

WORKDIR /opt/bitnami/heapster
USER 1001
ENTRYPOINT ["/opt/bitnami/heapster/bin/heapster"]
