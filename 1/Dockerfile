FROM bitnami/minideb as development

ARG HEAPSTER_VERSION=1.5.2
ARG GO_VERSION=1.9.4

RUN install_packages wget ca-certificates git make tar wget

RUN wget -nc https://dl.google.com/go/go$GO_VERSION.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf go$GO_VERSION.linux-amd64.tar.gz

ENV GOPATH=/
ENV PATH=$GOPATH/bin:/usr/local/go/bin:$PATH

RUN mkdir -p /src/k8s.io/ && \
    go get github.com/tools/godep && \
    cd /src/k8s.io/ && \
    git clone -b v${HEAPSTER_VERSION} --depth 1 https://github.com/kubernetes/heapster.git && \
    cd heapster && \
    make

FROM bitnami/minideb:jessie
LABEL maintainer "Bitnami <containers@bitnami.com>"

COPY --from=development /src/k8s.io/heapster/heapster /src/k8s.io/heapster/eventer /opt/bitnami/heapster/bin/
COPY --from=development /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/ca-certificates.crt
COPY --from=development /src/k8s.io/heapster/LICENSE /opt/bitnami/heapster/LICENSE

ENV PATH="/opt/bitnami/heapster/bin:$PATH"
EXPOSE 8082
WORKDIR    /opt/bitnami/heapster
USER 1001
ENTRYPOINT [ "/opt/bitnami/heapster/bin/heapster" ]
