FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html
COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY appcode/index.html /usr/share/nginx/html/index.html
COPY appcode/nginx.conf /etc/nginx/conf.d/default.conf

COPY appcode/ /usr/share/nginx/html/

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
