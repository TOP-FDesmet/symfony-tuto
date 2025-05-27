FROM php:8.3-fpm-alpine3.18

RUN apk update && apk add --no-cache \
    bash \
    curl \
    git \
    libzip-dev \
    nodejs \
    npm \
    openssl \
    postgresql-dev \
    unzip \
    vim \
    yarn \
    zip \
    # PHP extensions
    && docker-php-ext-install pdo_pgsql pgsql \
    # Composer
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

CMD ["php-fpm"]