#STAGE 1--> unzipping schema files
# Pull ubuntu 22.04 base image
FROM ubuntu:22.04 AS builder
  
# Install zip package
RUN apt-get update; \
    apt-get install -y zip

# Directory to copy catalogue code
RUN mkdir catalogue

WORKDIR /catalogue

# Copy the code for database schema
COPY ../../Source-Code/catalogue/catalogue.zip .

# unzip schema code 
RUN unzip catalogue.zip

# Directory to copy user code
RUN mkdir user

WORKDIR /user

# Copy the code for database schema
COPY ../../Source-Code/user/user.zip .

# unzip schema code 
RUN unzip user.zip


# STAGE 2 --> placing unzipped files in final image
# Pull mongodb image
FROM mongo

# Copy the unzipped schema code to mongodb for catalogue entrypoint 
COPY --from=builder /catalogue/schema/catalogue.js  /docker-entrypoint-initdb.d/

# Copy the unzipped schema code to mongodb for user entrypoint 
COPY --from=builder /user/schema/user.js  /docker-entrypoint-initdb.d/

# Expose port to listen on
EXPOSE 27017

# Make mongodb accept connection from any IP
CMD mongod --bind_ip 0.0.0.0



