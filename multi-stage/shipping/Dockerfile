FROM almalinux AS build
WORKDIR /opt/shipping
COPY pom.xml /opt/shipping/
COPY src /opt/shipping/src/
RUN yum update -y \
        && yum install maven -y \
        && mvn dependency:resolve \
        && mvn package

# FROM mcr.microsoft.com/java/jre:8u252-zulu-alpine
# WORKDIR /opt/shipping
# ENV CART_ENDPOINT=cart:8080
# ENV DB_HOST=mysql
# COPY --from=build /opt/shipping/target/shipping-1.0.jar shipping.jar
# CMD [ "java", "-Xmn256m", "-Xmx768m", "-jar", "shipping.jar" ]
# #
# # Build
# #
# FROM debian:10 AS build

# RUN apt-get update && apt-get -y install maven

# WORKDIR /opt/shipping

# COPY pom.xml /opt/shipping/
# RUN mvn dependency:resolve
# COPY src /opt/shipping/src/
# RUN mvn package

# #
# # Run
# #
# FROM openjdk:8-jdk

# EXPOSE 8080

# WORKDIR /opt/shipping

# ENV CART_ENDPOINT=cart:8080
# ENV DB_HOST=mysql

# COPY --from=build /opt/shipping/target/shipping-1.0.jar shipping.jar

# CMD [ "java", "-Xmn256m", "-Xmx768m", "-jar", "shipping.jar" ]

