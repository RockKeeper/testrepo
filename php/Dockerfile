# By Sharon Campbell and Ken Simon for Heptio

# https://docs.docker.com/engine/reference/builder/

# base this image on the PHP image that comes with Apache https://hub.docker.com/_/php/
FROM php:7.0-apache

# install mysql-client and curl for our data init script
# install the PHP extension pdo_mysql for our connection script
# clean up
RUN apt-get update \
  && apt-get install -y curl \
  && apt-get clean \
  && rm -rf /var/cache/apt/archives

# take the contents of the local html/ folder, and copy to /var/www/html/ inside the container
# this is the expected web root of the default website for this server, so put your index.php here
COPY html/ /var/www/html/
