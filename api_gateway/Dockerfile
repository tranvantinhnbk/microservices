FROM nginx:perl

COPY nginx.conf /etc/nginx/nginx.conf
COPY cert/server.crt /etc/nginx/ssl/server.crt
COPY cert/server.key /etc/nginx/ssl/server.key


COPY index.html /usr/share/nginx/html/index.html

EXPOSE 80
EXPOSE 443

CMD ["nginx", "-g", "daemon off;"]
