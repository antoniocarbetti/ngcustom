FROM nginx:latest
#configuration
COPY ./nginx.conf /etc/nginx/nginx.conf
#content, comment out the ones you dont need!
copy ./*.html /usr/share/nginx/html/
copy ./*.jpg /usr/share/nginx/html/
copy ./*.png /usr/share/nginx/html/
copy ./*.js /usr/share/nginx/html/

WORKDIR /app
RUN chown -R nginx:nginx /app && chmod -R 755 /app
RUN chown -R nginx:nginx /var/cache/nginx && chmod -R 755 /var/cache/nginx
RUN chown -R nginx:nginx /var/log/nginx
RUN chown -R nginx:nginx /etc/nginx/conf.d
RUN mkdir -p /var/cache/nginx/client_temp && chmod 755 /var/cache/nginx/client_temp
RUN mkdir -p /var/cache/nginx/proxy_temp && chmod 755 /var/cache/nginx/proxy_temp
RUN mkdir -p /var/cache/nginx/fastcgi_temp && chmod 755 /var/cache/nginx/fastcgi_temp

RUN touch /var/run/nginx.pid && chown -R nginx:nginx /var/run/nginx.pid
USER nginx
CMD ["nginx", "-g", "daemon off;"]
