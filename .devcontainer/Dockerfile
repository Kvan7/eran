FROM mcr.microsoft.com/devcontainers/base:bullseye

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
	&& apt-get -y install --no-install-recommends \
	m4 \
	build-essential \
	cmake \
	git \
	autoconf \
	libtool \
	texlive-latex-base \
	libboost-all-dev \
	libeigen3-dev \
	libgflags-dev \
	libgoogle-glog-dev \
	libopencv-dev \
	libprotobuf-dev \
	protobuf-compiler \
	python3-dev \
	python3-pip \
	python3-setuptools \
	python3-wheel \
	&& apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

RUN wget https://github.com/Kitware/CMake/releases/download/v3.19.7/cmake-3.19.7-Linux-x86_64.sh \
	&& bash ./cmake-3.19.7-Linux-x86_64.sh --skip-license \
	&& rm /usr/bin/cmake \
	&& ln -s ./cmake-3.19.7-Linux-x86_64/bin/cmake /usr/bin/cmake


