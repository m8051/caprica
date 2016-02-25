# Pick up the nginx base image
FROM m8051/adverts:base

# Author name
MAINTAINER "Jordi Garcia" <crawler8086@gmail.com>

# Install packages
RUN apt-get update
RUN apt-get -y install nginx

# Add the command to run at the start of the container
COPY ./config/nginx.conf /etc/nginx/nginx/nginx.conf
COPY ./config/sites-available/nginx_status /etc/nginx/sites-available/nginx_status

# Setup basic
# CMD ["ln -s /etc/nginx/sites-available/nginx_status /etc/nginx/sites-enabled/"]

# Only one CMD instruction is allowed in a Dockerfile
CMD ["nginx", "-g", "daemon off;"]
