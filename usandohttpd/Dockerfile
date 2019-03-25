FROM httpd:latest

ENV app="WebServer"
LABEL version="1.0.0"

RUN mkdir /opt/webserver
COPY ./giropops /opt/webserver/.

WORKDIR /usr/local/apache2/htdocs

COPY ./index.html /usr/local/apache2/htdocs/.

VOLUME /usr/local/apache2/htdocs/
EXPOSE 80

