FROM php:7-apache
RUN docker-php-ext-install pdo pdo_mysql
RUN apt-get update -y && apt-get install -y libpng-dev apache2-doc apache2-utils phpmyadmin libapache2-mod-fcgid apache2-suexec-pristine php-pear php-auth mcrypt  imagemagick libruby libapache2-mod-python memcached  php-gettext

RUN a2enmod suexec rewrite ssl actions include cgi
RUN a2enmod dav_fs dav auth_digest headers
RUN service apache2 restart
