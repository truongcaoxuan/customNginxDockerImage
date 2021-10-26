FROM nginx:latest

RUN rm /etc/nginx/conf.d/default.conf

COPY files/nginx.conf /etc/nginx/conf.d/default.conf

COPY files/index.html /usr/share/nginx/html
