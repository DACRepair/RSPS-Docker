FROM java:alpine

RUN apk update && \
    apk add git

VOLUME /usr/src/myapp
WORKDIR /usr/src/myapp

RUN mkdir /tmp/git
RUN git clone https://github.com/DACRepair/RSPS-Docker.git /tmp/git
RUN mv /tmp/git/Server/* /usr/src/myapp
RUN rm -rf /tmp/git

RUN ln -s /usr/src/myapp/Data /usr/src/myapp/data
RUN ln -s /usr/src/myapp/Data/CFG /usr/src/myapp/Data/cfg

CMD ["java", "-server", "-Xmx1024m", "-cp", "\"bin:libs/*:\"", "redone.Server"]