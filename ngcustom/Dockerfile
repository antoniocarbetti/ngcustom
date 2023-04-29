FROM nginxinc/nginx-unprivileged:1.20
#configuration
copy ./nginx.conf /etc/nginx/nginx.conf
#content, comment out the ones you dont need!
copy ./*.html /usr/share/nginx/html/
copy ./*.jpg /usr/share/nginx/html/
copy ./*.png /usr/share/nginx/html/
copy ./*.js /usr/share/nginx/html/
