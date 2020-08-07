FROM amazonlinux:latest

LABEL description="Dockerfile is intended to provision an environment with AWS CLI and Configuration in place"
LABEL maintainer="Engineering Department"

RUN yum update -y \
    && yum install -y unzip \
    && curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && ./aws/install --install-dir /usr/local/aws-cli --bin-dir /usr/local/bin \
    && rm awscliv2.zip \
    && aws --version

RUN mkdir -p ~/.aws

COPY credentials ~/.aws/credentials
COPY config ~/.aws/config

ENTRYPOINT ["tail", "-f", "/dev/null"]