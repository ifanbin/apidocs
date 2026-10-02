# Base image for the swaggerdocs Spring Boot 2.0.2 project.
# The project targets Java 1.8, so we install JDK 8 (Spring Boot 2.0.x and
# springfox 2.2.2 do not run on modern JDKs) plus Maven for builds.
FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        openjdk-8-jdk \
        maven \
        git \
        curl \
        ca-certificates \
    && rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
ENV PATH="${JAVA_HOME}/bin:${PATH}"

USER ubuntu
