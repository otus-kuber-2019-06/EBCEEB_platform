ARG base_image=nginx:stable

FROM $base_image

LABEL \
    base_image=$base_image

COPY [ "default.conf", "/etc/nginx/conf.d/default.conf" ]
COPY [ "index.html", "/app/index.html" ]
