FROM java:alpine
COPY app/ /usr/src/myapp/
WORKDIR /usr/src/myapp

RUN ln -s /usr/src/myapp/Data /usr/src/myapp/data
RUN ln -s /usr/src/myapp/Data/CFG /usr/src/myapp/Data/cfg

RUN du -h /usr/src/myapp

CMD ["java", "-server", "-Xmx1024m", "-cp", "\"bin:libs/*:\"", "redone.Server"]