FROM kanyi/circleci-gcloud-dev

# ensure local python is preferred over distribution python
ENV PATH /usr/local/bin:$PATH

# make some useful symlinks that are expected to exist
RUN cd /usr/local/bin \
	&& ln -s idle3 idle \
	&& ln -s pydoc3 pydoc \
	&& ln -s python3 python \
	&& ln -s python3-config python-config



