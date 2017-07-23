FROM java:8-jdk-alpine
RUN apk update && \
    apk add git

VOLUME /usr/src/myapp
WORKDIR /usr/src/myapp

RUN mkdir /tmp/git
RUN git clone https://github.com/DACRepair/RSPS-Docker.git /tmp/git
RUN mv /tmp/git/FileServer/* /usr/src/myapp
RUN rm -rf /tmp/git

EXPOSE 80/tcp 43595/tcp 43596/tcp

CMD ["java", "-cp", "\"bin:assets/*:\"", "org.apollo.jagcached.FileServer"]