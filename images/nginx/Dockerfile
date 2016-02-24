FROM m8051/adverts:nginx

COPY ./config/nginx.conf /etc/nginx/nginx/nginx.conf
COPY ./config/sites-available/nginx_status /etc/nginx/sites-available/nginx_status

CMD ["ln -s /etc/nginx/sites-available/nginx_status /etc/nginx/sites-enabled/"]
CMD ["nginx", "-g", "daemon off;"]
