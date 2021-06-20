FROM debian:buster

RUN apt-get update
RUN apt-get -y upgrade
RUN apt-get install -y php-fpm php-mysql php-mbstring php-gd redis-server php-redis php-xml wget vim
EXPOSE 9000
COPY ./conf/ /var/www/
RUN chmod +x /var/www/wordpress_php.sh
ENTRYPOINT [ "/var/www/wordpress_php.sh" ]
CMD [ "/usr/sbin/php-fpm7.3", "--nodaemonize" ]