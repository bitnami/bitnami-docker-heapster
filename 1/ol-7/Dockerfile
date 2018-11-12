FROM bitnami/oraclelinux-extras:7-r166 as buildenv

RUN install_packages ca-certificates wget
RUN wget -nc -P /tmp/bitnami/pkg/cache/ https://downloads.bitnami.com/files/stacksmith/heapster-1.5.4-1-linux-x86_64-ol-7.tar.gz && \
    echo "256040d40ae878ee440e1a0d953d411b95af468b0319129502b515d0595eb925  /tmp/bitnami/pkg/cache/heapster-1.5.4-1-linux-x86_64-ol-7.tar.gz" | sha256sum -c - && \
    tar -zxf /tmp/bitnami/pkg/cache/heapster-1.5.4-1-linux-x86_64-ol-7.tar.gz -P --transform 's|^[^/]*/files|/opt/bitnami|' --wildcards '*/files' && \
    rm -rf /tmp/bitnami/pkg/cache/heapster-1.5.4-1-linux-x86_64-ol-7.tar.gz

##################

FROM bitnami/oraclelinux-extras:7-r166
LABEL maintainer "Bitnami <containers@bitnami.com>"

COPY --from=buildenv /opt/bitnami/heapster /opt/bitnami/heapster
ENV BITNAMI_APP_NAME="heapster" \
    BITNAMI_IMAGE_VERSION="1.5.4-ol-7-r96" \
    PATH="/opt/bitnami/heapster/bin:$PATH"

RUN install_packages ca-certificates

EXPOSE 8082

WORKDIR /opt/bitnami/heapster
USER 1001
ENTRYPOINT [ "/opt/bitnami/heapster/bin/heapster" ]
