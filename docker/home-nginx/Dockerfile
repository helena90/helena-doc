FROM nginx:latest

USER root

RUN mkdir -p /var/www/www
RUN mkdir -p /var/www/blog
RUN mkdir -p /var/www/certbot
RUN mkdir -p /etc/letsencrypt

RUN chown nginx:nginx /var/www
RUN chown nginx:nginx /var/www/www
RUN chown nginx:nginx /var/www/blog
RUN chown nginx:nginx /var/www/certbot
RUN chown nginx:nginx /etc/letsencrypt

ADD ./nginx/nginx.conf /etc/nginx/nginx.conf