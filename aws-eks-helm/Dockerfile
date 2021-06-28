FROM alpine/helm

RUN apk add --update --no-cache git py-pip bash jq curl \
    && pip install awscli \
    && curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"  \
    && chmod +x /apps/kubectl && mv /apps/kubectl /usr/bin/  \
    && curl -o aws-iam-authenticator https://amazon-eks.s3.us-west-2.amazonaws.com/1.19.6/2021-01-05/bin/linux/amd64/aws-iam-authenticator \
    && chmod +x aws-iam-authenticator && mv aws-iam-authenticator /usr/bin \
    && curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp \
    && mv /tmp/eksctl /usr/local/bin


# RUN helm init \
#     && helm plugin install https://github.com/databus23/helm-diff --version master \
#     && helm plugin install https://github.com/futuresimple/helm-secrets --version master \
#     && helm plugin install https://github.com/aslafy-z/helm-git --version master \
#     && rm -f /var/cache/apk/*

ENTRYPOINT ["/bin/bash","-c"]