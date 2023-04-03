FROM registry.suse.com/bci/bci-base:15.4  
LABEL maintainer="JJ" 
RUN  zypper --non-interactive refresh && zypper --non-interactive install nginx 1.23.2
COPY files/default /etc/nginx/sites-available/default
COPY files/index.html /usr/share/nginx/html/index.html
EXPOSE 80
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
