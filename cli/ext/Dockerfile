ARG PHP_VERSION
ARG PHP_EXTENSION

FROM ghcr.io/peip-container/php-cli/base:${PHP_VERSION}

RUN install-php-extensions ${PHP_EXTENSION} ; \
    # strip debug symbols from extensions to reduce size
    find /usr/local/lib/php/extensions -name "*.so" -exec strip --strip-debug {} \;;
