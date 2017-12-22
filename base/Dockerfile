FROM ubuntu:16.04

LABEL maintainer "stephenkanyi@gmail.com"

## This Dockerfile is from https://hub.docker.com/r/remie/circleci-docker-gcloud/

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update -y; \
	apt-get install -y \
	apt-utils \
	unzip \
	python \
	npm \
	python3 \
	git \
	curl \
	&& curl -fsSL get.docker.com | /bin/sh; \
	curl -fsSLO https://dl.google.com/dl/cloudsdk/channels/rapid/google-cloud-sdk.zip; \
	unzip google-cloud-sdk.zip; \
	rm google-cloud-sdk.zip; \
	google-cloud-sdk/install.sh --usage-reporting=true --path-update=true --bash-completion=true --rc-path=/.bashrc --additional-components kubectl alpha beta; \
	google-cloud-sdk/bin/gcloud config set --installation component_manager/disable_update_check true;

ENV PATH /google-cloud-sdk/bin:$PATH

CMD ["/bin/bash"]