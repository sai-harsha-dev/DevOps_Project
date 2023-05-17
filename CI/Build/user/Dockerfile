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
COPY ../Source-code/user/user.zip .

# unzip source-code
RUN unzip user.zip 

# Remove original zip file
RUN rm -f user.zip


# STAGE 2 --> placing unzipped files in final image
# Pull node image
FROM node:current-alpine3.16

# Create new user to run application as non root
RUN adduser --disabled-password  application; \
    su application

# Copy the source code to container
COPY --from=builder /app .

# Install dependencies
RUN npm install
    
# Start server
CMD node server.js





    








