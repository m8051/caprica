# Pick up the ubuntu base image
FROM m8051/adverts:base

# Author name
MAINTAINER "Jordi Garcia" <crawler8086@gmail.com>

# Install packages
RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LC_ALL en_US.UTF-8

RUN apt-get update -qqy && apt-get install -qqy software-properties-common python-software-properties

# Install php7 packages
RUN LC_ALL=en_US.UTF-8 add-apt-repository -y ppa:ondrej/php && apt-get update -qqy && \
	apt-get install -qqy \
	php7.0-fpm \
	php7.0-cli \
	php7.0-common \
	php7.0-curl \
	php7.0-json \
	php7.0-gd \
	php7.0-mcrypt \
	php7.0-odbc \
	php7.0-pgsql \
	php7.0-mysql \
	php7.0-xmlrpc \
	php7.0-opcache \
	php7.0-intl \
	php7.0-bz2

RUN mkdir -p /var/www/html
RUN mkdir -p /run/php/


COPY ./config/www.conf /etc/php/7.0/fpm/pool.d/www.conf
COPY ./config/php-fpm.conf /etc/php/7.0/fpm/php-fpm.conf
COPY ./code/index.php /var/www/index.php

# Only one CMD instruction is allowed in a Dockerfile
CMD ["/usr/sbin/php-fpm7.0"]
