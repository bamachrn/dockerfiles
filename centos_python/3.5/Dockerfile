FROM registry.centos.org/eclipse/centos-jre:latest

MAINTAINER Dharmit Shah <dshah@redhat.com>

RUN sudo yum -y update && \
    sudo yum -y install centos-release-scl && \
    sudo yum -y install rh-python35 && \
    sudo yum clean all


# http://bugs.python.org/issue19846 # > At the moment, setting "LANG=C" on a Linux system *fundamentally breaks Python 3*, and that's not OK. 
ENV LANG C.UTF-8 

EXPOSE 8080 

WORKDIR /projects

CMD tailf /dev/null
