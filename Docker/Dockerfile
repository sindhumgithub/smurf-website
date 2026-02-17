FROM nginx:alpine

# Copy website files
COPY appcode/index.html /usr/share/nginx/html/index.html

# Copy nginx configuration
COPY appcode/nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
