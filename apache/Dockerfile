ARG APACHE_VERSION=""
FROM httpd:${APACHE_VERSION:+${APACHE_VERSION}-}alpine

RUN apk update; \
    apk upgrade;

# Create Directory to support multiple vhosts
RUN mkdir /usr/local/apache2/conf/vhosts

# Add config option to Apache to read all vhost config files in that folder
RUN echo "Include /usr/local/apache2/conf/vhosts" \
    >> /usr/local/apache2/conf/httpd.conf
