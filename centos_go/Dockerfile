FROM registry.centos.org/eclipse/centos_jre

MAINTAINER Dharmit Shah <dshah@redhat.com>

RUN sudo yum -y update && sudo yum -y install golang
RUN sudo mkdir -p /go/src /go/bin && sudo chmod -R 777 /go

RUN sed -i '$ d' /home/user/.bashrc
ENV GOPATH /go
ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH

EXPOSE 8080

CMD tail -f /dev/null
