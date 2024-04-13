FROM openjdk:11-jre-slim

ARG BUILD_NUMBER
ENV BUILD_NUMBER $BUILD_NUMBER

# Set the working directory
WORKDIR /app

# Copy the application JAR file and output log file into the container
COPY hello-$BUILD_NUMBER.tar.gz /app/

# Extract the contents of the tar.gz archive
RUN tar -xzf hello-$BUILD_NUMBER.tar.gz

# Set the command to run the application
CMD ["sh", "-c", "java -jar /app/target/hello-${BUILD_NUMBER}.jar"]
