#STAGE 1 --> unzipping sourcecode files
# Pull ubuntu 22.04 base image
FROM ubuntu:22.04 AS builder

# Install zip package
RUN apt-get update; \
    apt-get install -y zip

# Directory to copy code
RUN mkdir app

# Set /app as working directory
WORKDIR /app

# Copy the code for user page
COPY ../Source-code/shipping/shipping.zip .

# unzip source-code
RUN unzip shipping.zip 

# Remove original zip file
RUN rm -f shipping.zip

#Install maven
RUN apt install -y maven

#Build the jar artifact
RUN mvn clean package

# STAGE 2 --> placing unzipped files in final image
# Pull node image
FROM gcr.io/distroless/java11-debian11

# Copy the source code to container
COPY --from=builder /app/target/shipping.jar .

# Execute jar file
CMD java -jar shipping.js





    








