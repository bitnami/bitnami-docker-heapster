FROM bitnami/minideb:stretch as buildenv

RUN install_packages ca-certificates wget
RUN wget -nc -P /tmp/bitnami/pkg/cache/ https://downloads.bitnami.com/files/stacksmith/heapster-1.5.4-1-linux-amd64-debian-9.tar.gz && \
    echo "fb393f2c0c72879936fa5a32acdc5ed35703ba9a293d520f06dc2602a5cd756b  /tmp/bitnami/pkg/cache/heapster-1.5.4-1-linux-amd64-debian-9.tar.gz" | sha256sum -c - && \
    tar -zxf /tmp/bitnami/pkg/cache/heapster-1.5.4-1-linux-amd64-debian-9.tar.gz -P --transform 's|^[^/]*/files|/opt/bitnami|' --wildcards '*/files' && \
    rm -rf /tmp/bitnami/pkg/cache/heapster-1.5.4-1-linux-amd64-debian-9.tar.gz

##################

FROM bitnami/minideb:stretch
LABEL maintainer "Bitnami <containers@bitnami.com>"

COPY --from=buildenv /opt/bitnami/heapster /opt/bitnami/heapster
ENV BITNAMI_APP_NAME="heapster" \
    BITNAMI_IMAGE_VERSION="1.5.4-debian-9-r112" \
    PATH="/opt/bitnami/heapster/bin:$PATH"

RUN install_packages ca-certificates

EXPOSE 8082

WORKDIR /opt/bitnami/heapster
USER 1001
ENTRYPOINT [ "/opt/bitnami/heapster/bin/heapster" ]
