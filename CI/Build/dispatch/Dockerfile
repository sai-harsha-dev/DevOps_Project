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
COPY ../Source-code/dispatch/dispatch.zip .

# unzip source-code
RUN unzip dispatch.zip 

# STAGE 2 --> placing unzipped files in final image
# Pull python image
FROM golang

# Copy the extracted files to container
COPY --from=builder /app/* .

# Install application
RUN go mod init dispatch

RUN go get

# Execute application file
CMD go build





    








