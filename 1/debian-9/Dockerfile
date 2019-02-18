FROM bitnami/minideb:stretch
LABEL maintainer "Bitnami <containers@bitnami.com>"

# Install required system packages and dependencies
RUN install_packages ca-certificates wget
RUN wget -nc -P /tmp/bitnami/pkg/cache/ https://downloads.bitnami.com/files/stacksmith/heapster-1.5.4-20-linux-amd64-debian-9.tar.gz && \
    echo "d1eed9c284e6f0cd3d9a74c8acce45634290819ca6c5d1fb319bf934a74ec6a8  /tmp/bitnami/pkg/cache/heapster-1.5.4-20-linux-amd64-debian-9.tar.gz" | sha256sum -c - && \
    tar -zxf /tmp/bitnami/pkg/cache/heapster-1.5.4-20-linux-amd64-debian-9.tar.gz -P --transform 's|^[^/]*/files|/opt/bitnami|' --wildcards '*/files' && \
    rm -rf /tmp/bitnami/pkg/cache/heapster-1.5.4-20-linux-amd64-debian-9.tar.gz

ENV BITNAMI_APP_NAME="heapster" \
    BITNAMI_IMAGE_VERSION="1.5.4-debian-9-r191" \
    PATH="/opt/bitnami/heapster/bin:$PATH"

EXPOSE 8082

WORKDIR /opt/bitnami/heapster
USER 1001
ENTRYPOINT [ "/opt/bitnami/heapster/bin/heapster" ]
