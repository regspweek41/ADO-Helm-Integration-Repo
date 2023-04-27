FROM openjdk:8-jdk-alpine
VOLUME /tmp
EXPOSE 8080
ADD target/*.jar app.jar
ENV JAVA_OPTS=""
ENTRYPOINT [ "sh", "-c", "java -javaagent:.jar $JAVA_OPTS  -Delastic.apm.service_name=my-service-name -Delastic.apm.secret_token=dSrzrtAy3wDhy2kVsM -Delastic.apm.server_url=https://2571c723b8e84b04ad56a84803be016c.apm.southeastasia.azure.elastic-cloud.com:443 -Delastic.apm.environment=my-environment -Delastic.apm.application_packages=org.example -Djava.security.egd=file:/dev/./urandom -jar /app.jar" ]

java -javaagent:/path/to/elastic-apm-agent-<version>.jar \
-Delastic.apm.service_name=my-service-name \
-Delastic.apm.secret_token=dSrzrtAy3wDhy2kVsM \
-Delastic.apm.server_url=https://2571c723b8e84b04ad56a84803be016c.apm.southeastasia.azure.elastic-cloud.com:443 \
-Delastic.apm.environment=my-environment \
-Delastic.apm.application_packages=org.example \
-jar my-service-name.jar