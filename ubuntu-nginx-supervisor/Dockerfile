FROM ubuntu:18.04

MAINTAINER gapgit

RUN apt-get update && \
    apt-get install -y \
            nginx \
            supervisor && \
    chown -R www-data:www-data /var/lib/nginx && \
    chown -R www-data:www-data /code && \
    rm /etc/nginx/sites-enabled/default && \
    echo "\ndaemon off;" >> /etc/nginx/nginx.conf

RUN mkdir -p /var/log/supervisor

CMD ["supervisord", "-n"]
