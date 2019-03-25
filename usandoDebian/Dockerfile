FROM debian:latest

RUN apt-get update
RUN apt-get install -y apache2
ENV APACHE_LOCK_DIR="/var/lock"
ENV APACHE_PID_FILE="/var/run/apache2.pid"
ENV APACHE_LOG_DIR="/var/log/apache2"


ENV app="WebServer"
LABEL version="1.0.0"

RUN mkdir /opt/webserver
COPY ./giropops /opt/webserver/.

WORKDIR /var/www/html/

COPY ./index.html /var/www/html/

VOLUME /var/www/html/
EXPOSE 80

ENTRYPOINT ["/usr/sbin/apachectl"]
CMD ["-D","FOREGROUND"]

