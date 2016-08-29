FROM registry.centos.org/dharmit/centos_jre

MAINTAINER Dharmit Shah <dshah@redhat.com>

RUN sudo yum -y update && \
    sudo yum -y install epel-release && \
    sudo yum -y install python-pip && \
    sudo pip install --upgrade pip && \
    sudo yum clean all

ENV LANG C.UTF-8

# ENV PYTHON_VERSION 2.7.5

# if this is called "PIP_VERSION", pip explodes with "ValueError: invalid truth value '<VERSION>'"
# ENV PYTHON_PIP_VERSION 8.1.2

# install "virtualenv", since the vast majority of users of this image will want it

RUN sudo pip install --no-cache-dir virtualenv
EXPOSE 8080

WORKDIR /projects

CMD tailf /dev/null
