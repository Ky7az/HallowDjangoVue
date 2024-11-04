FROM nginx:1.27.2-alpine

COPY ./hallow.conf /etc/nginx/conf.d/hallow.conf

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]