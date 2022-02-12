FROM ubuntu:22.04
ARG DEBIAN_FRONTEND=noninteractive
RUN apt update && apt install -y apache2 vim && apt autoremove -y && apt clean
EXPOSE 80
COPY ./index.html /var/www/html/
RUN service apache2 start
CMD ["apachectl", "-D", "FOREGROUND"]
