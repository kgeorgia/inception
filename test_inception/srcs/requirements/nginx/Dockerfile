FROM debian:buster

RUN apt-get update
RUN apt-get -y upgrade
RUN apt-get install -y openssl php-gd php-xml vim nginx
EXPOSE 443
COPY ./conf/ /var/www/
#RUN chmod +x /var/www/nginx.sh
#ENTRYPOINT ["/var/www/nginx.sh"]
CMD ["nginx", "-g", "deamon off;"]