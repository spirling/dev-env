FROM php:7.4-fpm

RUN apt-get update && apt-get install -y --no-install-recommends  \
    cron \
    curl \
    git  \
    jq \
    libedit-dev \
    libfreetype6-dev \
    libicu-dev \
    libjpeg62-turbo-dev \
    libmcrypt-dev \
    libpng-dev  \
    libpspell-dev \
    libxml2-dev \
    libxslt-dev \
    libyaml-dev \
    libzip-dev \
    zip \
    zlib1g-dev \

RUN docker-php-ext-install opcache \
    && docker-php-ext-install bcmath \
    && docker-php-ext-install calendar \
    && docker-php-ext-install exif \
    && docker-php-ext-install mysqli \
    && docker-php-ext-install pcntl \
    && docker-php-ext-install pdo_mysql \
	&& docker-php-ext-install pspell \
    && docker-php-ext-install shmop \
    && docker-php-ext-install soap \
    && docker-php-ext-install sockets \
    && docker-php-ext-install sysvmsg \
    && docker-php-ext-install sysvsem \
    && docker-php-ext-install sysvshm \
    && docker-php-ext-install xml \
    && docker-php-ext-install zip \
    && docker-php-ext-install gettext \
    && docker-php-ext-configure intl \
    && docker-php-ext-install intl

RUN pecl install yaml && docker-php-ext-enable yaml

WORKDIR /var/www

CMD ["php-fpm"]