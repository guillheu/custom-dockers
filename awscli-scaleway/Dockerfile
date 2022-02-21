FROM amazon/aws-cli:latest

RUN yum install -y python3
RUN yum install -y jq

RUN pip3 install awscli awscli-plugin-endpoint boto3

RUN aws configure set plugins.endpoint awscli_plugin_endpoint
COPY aws-config /root/.aws/config

ENTRYPOINT aws configure && aws s3 ls && /bin/bash
