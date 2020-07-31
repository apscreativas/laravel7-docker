FROM php:7.3-cli-stretch

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# system dependencies
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    apt-utils \
    libxml2-dev \
    libpng-dev \
    libcurl4-openssl-dev \
    libzip-dev \
    file \
    g++ \
    make \
    uuid-runtime \
    git \
    zip \
    unzip

# php extensions
RUN docker-php-ext-install -j$(nproc) dom gd simplexml xml pdo_mysql curl mbstring opcache zip

# apache config
ENV APACHE_DOCUMENT_ROOT /var/www/html/public

WORKDIR /var/www/html

# command
CMD ["/usr/local/bin/php"]
