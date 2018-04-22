# Start with a base image containing Java runtime
FROM java:8

# Add Maintainer Info
LABEL maintainer="SKP"

# Add a volume pointing to /tmp
VOLUME /tmp


# Add the application's jar to the container
ADD config-git-server-0.0.1-SNAPSHOT.jar config-git-server.jar

RUN bash -c 'touch /config-git-server.jar'
# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/config-git-server.jar"]

EXPOSE 8080
EXPOSE 443
