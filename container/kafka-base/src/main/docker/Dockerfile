FROM rta/java8

# Python
ENV PYTHON_VERSION="2.7.9-1"
ENV PYTHON_PIP_VERSION="8.1.2"

# Confluent
ENV SCALA_VERSION="2.11"
ENV CONFLUENT_MAJOR_VERSION="3"
ENV CONFLUENT_MINOR_VERSION="2"

RUN yum update -y \
    && yum install -y epel-release \
    && yum install -y nc python-pip \
    && pip install --no-cache-dir --upgrade pip \
    && pip install --no-cache-dir jinja2 requests

RUN rpm --import http://packages.confluent.io/rpm/3.2/archive.key
COPY config/confluent.repo /etc/yum.repos.d/confluent.repo

COPY include/dub /usr/local/bin/dub
COPY include/cub /usr/local/bin/cub
COPY include/etc/confluent/docker /etc/confluent/docker