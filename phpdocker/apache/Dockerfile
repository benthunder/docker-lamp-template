FROM httpd:2.4

RUN mkdir -p /usr/local/apache2/sites-available
RUN mkdir -p /usr/local/apache2/htdocs/laraveldemo
RUN mkdir -p /usr/local/apache2/htdocs/wordpressdemo

COPY ./httpd.conf /usr/local/apache2/conf/httpd.conf 
COPY ./laraveldemo.conf /usr/local/apache2/sites-available/laraveldemo.conf
COPY ./wordpressdemo.conf /usr/local/apache2/sites-available/wordpressdemo.conf 
COPY ./vhosts.conf /usr/local/apache2/conf/extra/httpd-vhosts.conf 