FROM php:8.2-fpm

# Installer les dépendances nécessaires
RUN apt-get update && apt-get install -y \
    curl \
    zip \
    unzip \
    git \
    nodejs \
    npm \
    libpng-dev \
    libonig-dev \
    libxml2-dev \
    libzip-dev \
    && docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd zip

# Configurer le dossier de travail
WORKDIR /var/www/html

# Exposer le port
EXPOSE 9000

# Démarrer PHP-FPM
CMD ["php-fpm"]