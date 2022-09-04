FROM php:7.3-apache

# put files
WORKDIR /var/www/html/
COPY ./src .

# config permission
RUN chown -R root:www-data /var/www/html
RUN chmod 750 /var/www/html
RUN find . -type f -exec chmod 640 {} \;
RUN find . -type d -exec chmod 750 {} \;

# add sticky bit to prevent delete files
RUN chmod +t -R /var/www/html/
RUN apt-get update -y
RUN apt-get install cowsay figlet toilet fortune wget -y
RUN ln -s /usr/games/cowsay /usr/bin/
RUN ln -s /usr/games/cowthink /usr/bin/
RUN ln -s /usr/games/fortune /usr/bin/

RUN echo '🥷: You are master of Command Injection now! b38e625204bd8d09089d3eacc3a9c862' > /secret_file
# setup flag
# RUN echo "CBJS{XXXXXXXXXXXXXXXXXXX}" > /8byxc78qy-secret.txt
