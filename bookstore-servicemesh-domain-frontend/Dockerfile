FROM docker.m.daocloud.io/openjdk:12-alpine

MAINTAINER icyfenix

ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    JAVA_OPTS="" \
    PORT=80 \
    PROFILES="default"

ADD *.jar /gateway.jar

ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar /gateway.jar --spring.profiles.active=$PROFILES"]

EXPOSE $PORT
