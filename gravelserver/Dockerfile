FROM httpd:2.4
VOLUME ["/usr/local/apache2/htdocs", "/usr/local/apache2/htdocs/tiles"]
COPY conf /usr/local/apache2/conf
ARG USER=wicked
ARG PASSWD=gravel
RUN echo $PASSWD | htpasswd -ci /usr/local/apache2/conf/.htpasswd $USER