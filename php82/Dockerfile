FROM php:8.2.4RC1-apache-bullseye

RUN apt-get -y update
RUN apt-get -y install git

RUN cp /etc/apache2/mods-available/rewrite.load /etc/apache2/mods-enabled/ && \
    cp /etc/apache2/mods-available/headers.load /etc/apache2/mods-enabled/

COPY --from=composer /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/