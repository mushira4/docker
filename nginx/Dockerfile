#selects the distro
FROM ubuntu

#sign-off the script
MAINTAINER ERIKY R KASHIVAGUI <mushira4@gmail.com>

#run the command
RUN apt-get update 
RUN apt-get install -y nginx

#add a file or directory to the container
ADD exemple /etc/nginx/sites-enabled/default

#link the nginx log file to the default docker log resoure
RUN ln -sf /dev/stdout /var/log/nginx/access.log #default log
#RUN ln -sf /dev/stderr /var/log/ningx/error.log  #error log

ADD ./docker_example/ /rails

WORKDIR /rails

EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]

