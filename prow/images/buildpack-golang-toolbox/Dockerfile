# Basic golang buildpack

FROM eu.gcr.io/kyma-project/test-infra/buildpack-golang:go1.12

# Install additional tools

RUN go get golang.org/x/tools/cmd/goimports  \
    golang.org/x/lint/golint \
    github.com/vektra/mockery \
    github.com/kisielk/errcheck && \
    GO111MODULE="on" go get sigs.k8s.io/kind@v0.5.1

COPY ./license-puller.sh /license-puller.sh
ENV LICENSE_PULLER_PATH=/license-puller.sh
