# Start from the WordPress image
FROM wordpress:php7.4

# Copy the WordPress files
COPY . /var/www/html

# Set the working directory
WORKDIR /var/www/html

# The container will run Apache in the foreground
CMD ["apache2-foreground"]
