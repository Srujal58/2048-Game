FROM ubuntu:22.04

RUN apt-get update

RUN apt-get update && apt-get install -y curl unzip nginx

RUN echo "daemon off;" >> /etc/nginx/nginx.conf

RUN curl -L -o /var/www/html/master.zip https://github.com/gabrielecirulli/2048/archive/refs/heads/master.zip \
    && cd /var/www/html/ && unzip master.zip && mv 2048-master/* . && rm -rf 2048-master master.zip


EXPOSE 80

CMD [ "/usr/sbin/nginx","-c" ,"/etc/nginx/nginx.conf"]
