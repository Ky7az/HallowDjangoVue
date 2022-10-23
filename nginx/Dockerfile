FROM nginx:1.22.1-alpine

COPY ./hallow.conf /etc/nginx/conf.d/hallow.conf

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]