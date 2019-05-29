FROM centos:7
MAINTAINER Liyong "liyong635@163.com"

RUN /bin/echo "HelloWorld"
RUN /bin/echo "root:123qwe"|chpasswd
RUN useradd liyong
RUN /bin/echo "liyong:123qwe"|chpasswd
RUN /bin/echo -e "LANG=\"en_US.UTF-8\"" > /etc/default/local
EXPOSE 22
EXPOSE 80
CMD /usr/sbin/sshd -D


