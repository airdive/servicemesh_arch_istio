FROM docker.m.daocloud.io/openjdk:12-alpine

MAINTAINER icyfenix

ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    JAVA_OPTS="" \
    PORT=80 \
    PROFILES="default"

ADD *.jar /bookstore-account.jar

ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar /bookstore-account.jar --spring.config.location=/config/application.yaml --spring.profiles.active=$PROFILES"]

EXPOSE $PORT
