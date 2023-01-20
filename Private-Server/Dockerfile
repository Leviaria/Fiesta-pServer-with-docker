FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y git && \
    apt-get install -y unzip && \
    apt-get install -y wget && \
    apt-get install -y apache2 && \
    apt-get install -y php && \
    apt-get install -y mysql-server && \
    apt-get install -y libapache2-mod-php

WORKDIR /var/www/html

RUN git clone https://github.com/FiestaOnlinePS/FiestaOnlinePS.git

WORKDIR /var/www/html/FiestaOnlinePS

RUN wget https://github.com/FiestaOnlinePS/FiestaOnlinePS/releases/download/v1.0.0/fiesta_online_server_1.0.0.zip

RUN unzip fiesta_online_server_1.0.0.zip

RUN mv server/* .

RUN rm fiesta_online_server_1.0.0.zip

RUN rm -r server

RUN chown -R www-data:www-data /var/www/html

EXPOSE 80

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
