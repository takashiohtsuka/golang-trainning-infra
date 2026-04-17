FROM mysql:8.0

RUN microdnf install -y make wget tar && \
    wget -q https://go.dev/dl/go1.24.2.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf go1.24.2.linux-amd64.tar.gz && \
    rm go1.24.2.linux-amd64.tar.gz && \
    microdnf clean all

ENV PATH=$PATH:/usr/local/go/bin:/root/go/bin

COPY golang-trainning-database/docker/init.sql /docker-entrypoint-initdb.d/
