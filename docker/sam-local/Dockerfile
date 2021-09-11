FROM node:lts-buster

WORKDIR /app

RUN apt-get update && apt-get install -y \
  curl    \
  git     \
  less    \
  netcat  \
  sudo    \
  unzip   \
  vim     \
  wget    \
  python3 \
  python3-pip \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

# install aws-cli
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
  && unzip awscliv2.zip \
  && rm -f awscliv2.zip \
  && aws/install \
  && rm -fr aws \
  # install aws-sam-cli
  && pip3 install aws-sam-cli \
  && npm install -g former2
