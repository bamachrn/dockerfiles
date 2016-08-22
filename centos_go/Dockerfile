FROM registry.centos.org/dharmit/centos_jre

RUN yum -y update && yum -y install golang
RUN mkdir -p /go/src /go/bin && chmod -R 777 /go

# ENV GOLANG_VERSION 1.6.2
# ENV GOLANG_DOWNLOAD_URL https://golang.org/dl/go$GOLANG_VERSION.linux-amd64.tar.gz
# ENV GOLANG_DOWNLOAD_SHA256 e40c36ae71756198478624ed1bb4ce17597b3c19d243f3f0899bb5740d56212a
# 
# RUN curl -fsSL "$GOLANG_DOWNLOAD_URL" -o golang.tar.gz \
#     && echo "$GOLANG_DOWNLOAD_SHA256  golang.tar.gz" | sha256sum -c - \
#     && tar -C /usr/local -xzf golang.tar.gz \
#     && rm golang.tar.gz

RUN sed -i '$ d' /home/user/.bashrc
ENV GOPATH /go
ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH

EXPOSE 8080

CMD tail -f /dev/null
