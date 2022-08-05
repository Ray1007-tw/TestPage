FROM openjdk:11.0.6-jre-slim
COPY ./ /
ENTRYPOINT ["java","-Dspring.config.location=file:/application.yml","-jar","demo.jar"]