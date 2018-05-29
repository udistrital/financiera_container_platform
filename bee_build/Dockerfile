FROM golang:1.8
ARG PROXY 
ARG USER_ID
ENV http_proxy $PROXY
ENV https_proxy $PROXY
RUN apt-get update && apt-get install -y sudo
ENV GOPATH /home/developer/go
ENV PATH /home/developer/go/bin:/usr/local/go/bin:$PATH
#USER developer
RUN mkdir -p /home/developer/go
RUN go get -u github.com/beego/bee && \
    go get -u github.com/astaxie/beego
WORKDIR $GOPATH