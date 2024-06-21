# Description: Dockerfile for http-server
FROM httpd:2.4

# Copy the files to the container
COPY ./public-html/ /usr/local/apache2/htdocs/
COPY ./httpd-config.conf /usr/local/apache2/conf/httpd.conf
