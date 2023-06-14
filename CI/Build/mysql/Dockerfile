#STAGE 1--> unzipping schema files
# Pull ubuntu 22.04 base image
FROM ubuntu:22.04 AS builder
  
# Install zip package
RUN apt-get update; \
    apt-get install -y zip

# Directory to copy shipping code
RUN mkdir shipping

WORKDIR /shipping

# Copy the code for database schema
COPY ../../Source-Code/shipping/shipping.zip .

# unzip schema code 
RUN unzip shipping.zip


# STAGE 2 --> placing unzipped files in final image
# Pull mongodb image
FROM mysql:5.7

# Copy the unzipped schema code to mysql for shipping entrypoint 
COPY --from=builder /shipping/schema/shipping.sql  /docker-entrypoint-initdb.d/

# Expose port to listen on
EXPOSE 3306




