# Base image
FROM wordpress:php7.4-apache
# Copy custom code, themes, and plugins
COPY . /var/www/html/
# Set the working directory
WORKDIR /var/www/html
# Expose port 80
EXPOSE 80
