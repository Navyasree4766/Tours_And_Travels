# Dockerfile — Apache + PHP 8.1
FROM php:8.1-apache

# Install PHP MySQL extensions
RUN docker-php-ext-install mysqli pdo pdo_mysql

# Copy project files to Apache directory
COPY . /var/www/html/

# Set proper permissions
RUN chown -R www-data:www-data /var/www/html \
 && chmod -R 755 /var/www/html

# Apache listens on port 80
EXPOSE 80

# Start Apache
CMD ["apache2-foreground"]

