FROM openjdk:11.0.6-jre-slim
COPY ./ /
EXPOSE 8087
 ENV JAVA_TOOL_OPTIONS "-Dcom.sun.management.jmxremote.ssl=false \
 -Dcom.sun.management.jmxremote.authenticate=false \
 -Dcom.sun.management.jmxremote.port=8087 \
 -Dcom.sun.management.jmxremote.rmi.port=8087 \
 -Dcom.sun.management.jmxremote.host=0.0.0.0 \
 -Djava.rmi.server.hostname=0.0.0.0 \
 -XX:+HeapDumpOnOutOfMemoryError \
 -XX:HeapDumpPath=/tmp"
ENTRYPOINT ["java","-Dspring.config.location=file:/application.yml","-jar","demo.jar"]