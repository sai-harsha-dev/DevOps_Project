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
COPY ../Source-code/payment/payment.zip .

# unzip source-code
RUN unzip payment.zip 

# STAGE 2 --> placing unzipped files in final image
# Pull python image
FROM gcr.io/distroless/python3-debian11

# Copy the requirements file to container
COPY --from=builder /app/requirements.txt .

# Copy the application file to container
COPY --from=builder /app/payment.ini

# Install requirements
RUN pip3 install -r requirements.txt

# Execute application file
CMD /usr/local/bin/uwsgi --ini payment.ini





    








