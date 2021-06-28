FROM alpine/helm

RUN apk add --update --no-cache git py-pip bash jq curl \
    && pip install awscli \
    && curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

# ADD https://storage.googleapis.com/kubernetes-release/release/$KUBECTL_VER/bin/linux/amd64/kubectl /usr/bin/kubectl
# RUN chmod +x /usr/bin/kubectl

# ADD https://github.com/roboll/helmfile/releases/download/${HELMFILE_VERSION}/helmfile_linux_amd64 /usr/bin/helmfile
# RUN chmod +x /usr/bin/helmfile


# RUN helm init \
#     && helm plugin install https://github.com/databus23/helm-diff --version master \
#     && helm plugin install https://github.com/futuresimple/helm-secrets --version master \
#     && helm plugin install https://github.com/aslafy-z/helm-git --version master \
#     && rm -f /var/cache/apk/*

ENTRYPOINT ["/bin/bash","-c"]