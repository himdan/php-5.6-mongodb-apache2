FROM ubuntu:20.04

RUN apt-get update && apt-get install -y software-properties-common

RUN LC_ALL=C.UTF-8 add-apt-repository -y ppa:ondrej/php

RUN apt-get update -y && apt-get install -y apache2 apache2-utils

RUN apt-get update -y && apt-get install -y php5.6 \
    php5.6-dev \
    libapache2-mod-php5.6 \
    php5.6-common \
    php5.6-mysql \
    php5.6-gmp \
    php5.6-ldap \
    php5.6-curl \
    php5.6-intl \
    php5.6-mbstring \
    php5.6-xmlrpc \
    php5.6-gd \
    php5.6-bcmath \
    php5.6-xml \
    php5.6-cli \
    php5.6-zip

RUN update-alternatives --set php /usr/bin/php5.6
RUN update-alternatives --set php-config /usr/bin/php-config5.6
RUN update-alternatives --set phpize /usr/bin/phpize5.6
RUN pecl channel-update pecl.php.net
RUN pecl install mongodb-1.7.4
RUN echo "extension=mongodb.so" >> `php --ini | grep "Loaded Configuration" | sed -e "s|.*:\s*||"`
RUN echo "extension=mongodb.so" >> /etc/php/5.6/apache2/php.ini
EXPOSE 80