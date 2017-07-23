FROM openjdk:alpine

VOLUME /usr/src/myapp
WORKDIR /usr/src/myapp

COPY app/ /usr/src/myapp


EXPOSE 80/tcp 43595/tcp 43596/tcp

ENTRYPOINT ["ls", "&&"]
CMD ["java", "-cp", "\"bin:assets/*:\"", "org.apollo.jagcached.FileServer"]