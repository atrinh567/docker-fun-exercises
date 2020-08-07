FROM nginx:latest

LABEL maintainer="Anthony Trinh"
LABEL app="Advanced Web Server"

ENV NGINX_PORT=80

COPY index.html /usr/share/nginx/html

EXPOSE 80

STOPSIGNAL SIGTERM

CMD ["nginx", "-g", "daemon off;"]