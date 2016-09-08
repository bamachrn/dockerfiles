FROM registry.centos.org/eclipse/centos_jre

MAINTAINER Dharmit Shah <dshah@redhat.com>

RUN sudo yum -y update && \
    sudo yum -y install epel-release && \
    sudo yum -y install python34 && \
    sudo yum clean all

RUN curl https://bootstrap.pypa.io/get-pip.py | sudo python3

# http://bugs.python.org/issue19846 # > At the moment, setting "LANG=C" on a Linux system *fundamentally breaks Python 3*, and that's not OK. 
# ENV LANG C.UTF-8 

# ENV PYTHON_VERSION 3.5.1 

# if this is called "PIP_VERSION", pip explodes with "ValueError: invalid truth value '<VERSION>'" 
# ENV PYTHON_PIP_VERSION 8.1.1 

# make some useful symlinks that are expected to exist 
RUN cd /usr/local/bin \
        && sudo ln -s easy_install-3.4 easy_install \
        # && sudo ln -s idle3 idle \
        && sudo ln -s pydoc3 pydoc \
        && sudo ln -s python3 python
        # && sudo ln -s python-config3 python-config

RUN sudo pip install --no-cache-dir virtualenv

EXPOSE 8080 

WORKDIR /projects

CMD tailf /dev/null
