FROM ubuntu:latest
RUN apt-get update && apt-get install -y nginx
ADD index.html /var/www/html/
CMD ["nginx", "-g", "daemon off;"]
