FROM nginx

RUN apt update
RUN apt install dnsutils -y
RUN apt install -y net-tools
RUN apt install -y tcpdump
RUN apt install telnet -y

COPY ./index.html /var/www/html/index.html

COPY ./index.html /usr/share/nginx/html/index.html

CMD ["nginx", "-g", "daemon off;"]
