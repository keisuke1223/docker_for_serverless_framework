FROM python:3.7-alpine
ARG AWS_ACCESS_KEY_ID
ARG AWS_SECRET_ACCESS_KEY

ENV NODE_PATH /usr/lib/node_modules/
# install nodejs
RUN apk update \
  && apk add --no-cache nodejs npm

# install aws-cli
RUN pip install awscli

RUN pip install requests

# install serverless framework
RUN npm install -g serverless \
  && npm install --save serverless-python-requirements

# set aws key
RUN sls config credentials --provider aws --key $AWS_ACCESS_KEY_ID --secret $AWS_SECRET_ACCESS_KEY

# change work directory
RUN mkdir -p /app
WORKDIR /app
