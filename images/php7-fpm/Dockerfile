# Pick up the ubuntu base image
FROM m8051/adverts:base

# Author name
MAINTAINER "Jordi Garcia" <crawler8086@gmail.com>

# Install packages
RUN apt-get update
RUN apt-get -y install software-properties-common python-software-properties
RUN apt-get -y install language-pack-en-base
RUN LC_ALL=en_US.UTF-8 add-apt-repository -y ppa:ondrej/php
RUN apt-get update
RUN apt-get -y install php7.0 php7.0-fpm php7.0-curl php7.0-mysql php7.0-cl php7.0-cgi php7.0-xsl php7.0-bz2 php7.0-json

# Only one CMD instruction is allowed in a Dockerfile
# CMD ["php7.0-fpm", "-g", "daemon off;"]
