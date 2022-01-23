ARG PHP_VERSION
ARG PHP_EXTENSION
ARG REPO_OWNER=peip-container

FROM ghcr.io/${REPO_OWNER}/php-cli/base:${PHP_VERSION}

RUN install-php-extensions ${PHP_EXTENSION} ; \
    # strip debug symbols from extensions to reduce size
    find /usr/local/lib/php/extensions -name "*.so" -exec strip --strip-debug {} \;;
