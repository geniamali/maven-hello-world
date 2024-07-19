FROM openjdk:8-jre-slim

RUN groupadd -r myappgroup && useradd -r -g myappgroup myappuser

WORKDIR /app

COPY --chown=myappuser:myappgroup myapp/target/*.jar myapp.jar

USER myappuser

ENTRYPOINT ["java", "-jar", "myapp.jar"]
