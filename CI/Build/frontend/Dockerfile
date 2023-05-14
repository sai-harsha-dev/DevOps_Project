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

# Copy the code for main page
COPY ../../Source-Code/catalogue/frontend.zip .

# unzip source-code
RUN unzip frontend.zip

# Remove original zip file
RUN rm frontend.zip



# STAGE 2 --> placing unzipped files in final image
# Pull nginx alpline image
FROM nginx:stable-alpine-slim

# Change working directory to /usr/share/nginx/html 
WORKDIR  /usr/share/nginx/html

# Remove default index.html
RUN rm index.html

# Place web page code in workdir
COPY --from=builder /app  .

# Load the configuration
CMD nginx -s reload



