FROM php:7.4-apache

RUN docker-php-ext-install pdo pdo_mysql mysqli json
RUN a2enmod rewrite

ENV DATABASE_USER=bookmedik
ENV DATABASE_PASSWORD=bookmedik
ENV DATABASE_HOST=db

EXPOSE 80

WORKDIR /var/www/html

COPY ./bookmedik /var/www/html
ADD script.sh /usr/local/bin/script.sh

RUN chmod +x /usr/local/bin/script.sh

CMD ["/usr/local/bin/script.sh"]
