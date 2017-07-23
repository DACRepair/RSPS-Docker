FROM java:alpine
COPY . /usr/src/myapp
WORKDIR /usr/src/myapp

CMD ["java", "-cp", "\"bin:assets/*:\"", "org.apollo.jagcached.FileServer"]