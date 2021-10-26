FROM centos:7

RUN yum install -y update \
    yum install -y sudo \
    yum install -y epel-release \
    yum install -y https://rpms.remirepo.net/enterprise/remi-release-7.rpm \
    yum clean all \
    yum install -y wget curl

RUN yum install -y httpd \
    yum install -y --enablerepo=remi-php74 php-xml php-soap php-xmlrpc \
                   php-mbstring php-json php-gd php-mcrypt php-mysql 

WORKDIR /var/www/html

ADD ./code /var/www/html

CMD ["/usr/sbin/httpd", "-D","FOREGROUND"]

EXPOSE 80
