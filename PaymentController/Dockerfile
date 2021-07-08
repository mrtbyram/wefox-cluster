FROM openjdk:8-jre-alpine

ENV APPLICATION_USER java
RUN adduser -D -g '' $APPLICATION_USER

RUN apk update && apk add bash coreutils
RUN apk add git
RUN mkdir /app
RUN chown -R $APPLICATION_USER /app

WORKDIR /app
RUN git clone https://github.com/mrtbyram/wefox.git

USER $APPLICATION_USER

CMD ["java", "-jar", "wefox/build/app.jar"]
