FROM java:alpine
COPY app/ /usr/src/myapp/
WORKDIR /usr/src/myapp

CMD ["java", "-cp", "\"bin:assets/*:\"", "org.apollo.jagcached.FileServer"]