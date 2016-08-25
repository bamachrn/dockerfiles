FROM registry.centos.org/dharmit/centos_jre

MAINTAINER Dharmit Shah <dshah@redhat.com>

RUN yum -y update && yum -y install golang
RUN mkdir -p /go/src /go/bin && chmod -R 777 /go

RUN sed -i '$ d' /home/user/.bashrc
ENV GOPATH /go
ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH

EXPOSE 8080

CMD tail -f /dev/null
