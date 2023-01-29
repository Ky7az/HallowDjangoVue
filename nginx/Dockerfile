FROM nginx:1.23.3-alpine

COPY ./hallow.conf /etc/nginx/conf.d/hallow.conf

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]