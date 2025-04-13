FROM nginx
RUN rm -rf /usr/share/nginx/html/index.html
#the content in the code keeping html dir
COPY nginx.conf /etc/nginx/nginx.conf
COPY code /usr/share/nginx/html/
