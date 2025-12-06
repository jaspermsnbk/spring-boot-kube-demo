# get base package from 17-jre-alpine 
FROM eclipse-temurin:25-jre-alpine

# get an argument when 'docker build' executed, 
# where JAR_FILE has the path of jar file (as shown in the next step)
ARG JAR_FILE
# verify the arguments 
RUN echo "JAR_FILE: ${JAR_FILE}"

# Open 8080 port for incomming traffic 
EXPOSE 8080 
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]