FROM php:fpm-alpine

ARG gid
ARG uid

RUN docker-php-ext-install bcmath mysqli pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

#RUN addgroup --gid "$gid" "devuser" \
#    && adduser \
#    --disabled-password \
#    --gecos "" \
#    --ingroup "devuser" \
#    --uid "$uid" \
#    "devuser" \
#    && addgroup "devuser" "www-data"

USER $uid:$gid

WORKDIR /home/devuser/app
