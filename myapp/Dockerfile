# Multistage dockerfile to package app with maven and run it

FROM maven:3.8.6-openjdk-8-slim as BUILDER
ARG VER
WORKDIR /app
COPY pom.xml ./
RUN mvn -B dependency:resolve
COPY src/ ./src
RUN mvn -B package

FROM openjdk:8-jre-slim
ARG VER
COPY --from=BUILDER /app/target/myapp-$VER.jar myapp.jar
RUN useradd kepler-alien
USER kepler-alien
CMD java -jar myapp.jar
