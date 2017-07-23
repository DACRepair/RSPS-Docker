FROM java:8-jdk-alpine

VOLUME /usr/src/myapp
WORKDIR /usr/src/myapp

COPY app/ /usr/src/myapp

RUN ln -s /usr/src/myapp/Data /usr/src/myapp/data
RUN ln -s /usr/src/myapp/Data/CFG /usr/src/myapp/Data/cfg

EXPOSE 43594 43594/udp

CMD ["java", "-server", "-Xmx1024m", "-cp", "\"bin:libs/*:\"", "redone.Server"]