# Pick up the ubuntu base image
FROM m8051/adverts:base

# Author name
MAINTAINER "Jordi Garcia" <crawler8086@gmail.com>

# Install packages
RUN apt-get update && apt-get -y install nginx

# Add the command to run at the start of the container
COPY ./config/nginx.conf /etc/nginx/nginx.conf
COPY ./config/vhost/caprica.conf /etc/nginx/sites-available/default

# Only one CMD instruction is allowed in a Dockerfile
CMD ["nginx", "-g", "daemon off;"]
