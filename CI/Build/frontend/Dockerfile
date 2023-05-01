# Pull nginx alpline image
FROM nginx:stable-alpine-slim

# Install zip package
RUN apk update; apk add zip

# Change working directory to /usr/share/nginx/html 
WORKDIR  /usr/share/nginx/html

# Copy source code to nginx root directory
COPY frontend.zip .

# Remove default index.html
RUN rm index.html

# Place frontend in root directory of nginx
RUN unzip frontend.zip



