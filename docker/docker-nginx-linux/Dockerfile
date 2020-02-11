FROM debian:buster-slim

RUN apt-get update \
    && apt-get install -yy nginx

RUN ln -sf /dev/stdout /var/log/nginx/access.log \
    && ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80

VOLUME [ "/usr/share/nginx/html" ]

CMD ["nginx", "-g", "daemon off;"]