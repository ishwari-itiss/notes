FROM ubuntu:latest

RUN apt-get update && apt-get install -y apache2

COPY reverse-proxy.conf /etc/apache2/sites-available/000-default.conf

RUN ln -s /etc/apache2/mods-available/proxy.load /etc/apache2/mods-enabled/ && \
    ln -s /etc/apache2/mods-available/proxy_http.load /etc/apache2/mods-enabled/

EXPOSE 80

CMD ["apache2ctl", "-D", "FOREGROUND"]
