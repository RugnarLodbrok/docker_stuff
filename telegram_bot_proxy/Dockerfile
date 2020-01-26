FROM nginx:alpine
RUN cp /etc/nginx/nginx.conf /etc/nginx/nginx.conf.cpy && \
    cat /etc/nginx/nginx.conf.cpy | sed 's/include \/etc\/nginx\/conf.d\/\*.conf;/\0\n    include \/mnt\/proxy.conf;/' > /etc/nginx/nginx.conf && \
    rm /etc/nginx/nginx.conf.cpy
CMD nginx -g "daemon off;"
