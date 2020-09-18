FROM php:7

RUN apt-get update -y && apt-get install -y openssl zip unzip git wget gnupg libmcrypt-dev libpng-dev libzip-dev

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash - && apt-get install -y nodejs

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN pecl install mcrypt-1.0.3
RUN docker-php-ext-install pdo pdo_mysql mysqli gd zip
RUN docker-php-ext-enable mcrypt

#RUN pecl install -o -f xdebug \
#    && rm -rf /tmp/pear \
#    && echo "zend_extension=/usr/local/lib/php/extensions/no-debug-non-zts-20121212/xdebug.so" > /usr/local/etc/php/conf.d/xdebug.ini \
 
RUN useradd --user-group --create-home --shell /bin/false app

ENV HOME=/home/app
ENV NODE_ENV=development

COPY ./app $HOME/

WORKDIR $HOME
#RUN mkdir ./app/storage
RUN chmod 777 storage/ -R

CMD bash -c "composer install && npm install && cp .env.example .env && php artisan serve --host 0.0.0.0 --port 8080 && php artisan migrate"
