FROM java:alpine
COPY . /usr/src/myapp
WORKDIR /usr/src/myapp

RUN ln -s /usr/src/myapp/Data /usr/src/myapp/data
RUN ln -s /usr/src/myapp/Data/CFG /usr/src/myapp/Data/cfg

CMD ["java", "-server", "-Xmx1024m", "-cp bin:libs/*:", "redone.Server"]