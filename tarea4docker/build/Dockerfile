FROM debian

RUN apt-get update && apt-get install -y apache2 libapache2-mod-php7.3 php7.3 php7.3-mysql php-xml php-gd php-mysql php-mbstring && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN rm /var/www/html/index.html && a2enmod rewrite

EXPOSE 80

COPY ./drupal /var/www/html

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
