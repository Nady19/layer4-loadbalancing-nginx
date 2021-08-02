FROM nginx
RUN apt update
RUN apt install dnsutils -y
RUN apt install -y net-tools
RUN apt install -y tcpdump
RUN apt install telnet -y

COPY nginx.conf /etc/nginx/nginx.conf

CMD ["nginx", "-g", "daemon off;"]
