FROM openjdk:8

COPY target/spring-boot-rest-example-0.5.0.war spring-boot-rest-example-0.5.0.war
EXPOSE 8090 8091 3306

RUN curl -O https://download.newrelic.com/newrelic/java-agent/newrelic-agent/current/newrelic.jar
ENV JAVA_OPTS="$JAVA_OPTS -javaagent:/newrelic.jar"

ENV NEW_RELIC_APP_NAME="springBoot"
ENV NEW_RELIC_LICENSE_KEY="3a354b72a6977462ab58b4cd8c49264aac5aNRAL"
ENTRYPOINT ["java", "-javaagent:/newrelic.jar", "-jar", "/spring-boot-rest-example-0.5.0.war"]
