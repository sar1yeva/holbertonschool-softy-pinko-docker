FROM nginx:latest

# Copy static website files
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Apply custom Nginx config
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf
