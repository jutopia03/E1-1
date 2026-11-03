FROM nginx:1.31-alpine
LABEL org.opencontainers.image.title="e1-custom-nginx" \
      org.opencontainers.image.authors="jutopia03"
ENV APP_ENV=dev
COPY site/ /usr/share/nginx/html/
EXPOSE 80
HEALTHCHECK --interval=10s --timeout=3s --retries=3 \
  CMD wget -q -O /dev/null http://localhost/ || exit 1