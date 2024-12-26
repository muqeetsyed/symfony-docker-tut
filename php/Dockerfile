FROM php:8.0-fpm


RUN apt-get update && apt-get install -y --no-install-recommends \
    git \
    zlib1g-dev \
    libxml2-dev \
    libpng-dev \
    libzip-dev \
    vim curl debconf subversion git apt-transport-https apt-utils \
    build-essential locales acl mailutils wget nodejs zip unzip \
    gnupg gnupg1 gnupg2 \
    sudo \
    ssh \
    default-mysql-client \
    libonig-dev \
    && docker-php-ext-install \
    pdo \
    pdo_mysql \
    soap \
    zip \
    opcache \
    gd \
    intl


RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN curl -sS https://get.symfony.com/cli/installer | bash
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
RUN chmod +x /usr/bin/composer
ENV COMPOSER_ALLOW_SUPERUSER 1

RUN mv /root/.symfony5/bin/symfony /usr/local/bin/symfony


WORKDIR /var/www/symfony_docker