FROM openjdk:8

COPY target/spring-boot-rest-example-0.5.0.war spring-boot-rest-example-0.5.0.war

# Download and install the New Relic Java Agent
RUN curl -O https://download.newrelic.com/newrelic/java-agent/newrelic-agent/current/newrelic.jar

EXPOSE 8090 8091 8092 3306

ENTRYPOINT ["java", "-javaagent:/newrelic.jar", "-Dnewrelic.config.license_key=3a354b72a6977462ab58b4cd8c49264aac5aNRAL", "-jar", "/spring-boot-rest-example-0.5.0.war"]

