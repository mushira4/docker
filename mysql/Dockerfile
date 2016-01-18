#selects distro
FROM ubuntu

#sign-off the script
MAINTAINER ERIKY R KASHIVAGUI <mushira4@gmail.com>

#Creates an environment variable
ENV DEBIAN_FRONTEND noninteractive

#installs the mysql-server
RUN apt-get update 
RUN apt-get install -y mysql-server-5.5

#Add the mysql config file
ADD my.cnf /etc/mysql/conf.d/my.cnf
RUN chmod 664 /etc/mysql/conf.d/my.cnf

ADD run /usr/local/bin/run
RUN chmod +x /usr/local/bin/run

#mount a data volume
VOLUME ["/var/lib/mysql"]

EXPOSE 3306

CMD ["/usr/local/bin/run"]


