FROM blalor/centos:latest

ADD prepare_container.sh /tmp/prepare_container.sh
ADD hosts                /tmp/hosts
ADD start.sh             /opt/start.sh
#ADD puppet/              /tmp/puppet

#RUN yum install -y --enablerepo=centosplus libselinux-devel libselinux

RUN yum update -y

RUN /bin/bash /tmp/prepare_container.sh;

RUN yum -y clean all

EXPOSE 22 80 8020 8080 9083 10000 11000 50070 50075 50111 
#TODO: EXPOSE ALL PORTS FOR EVERY SERVICE

CMD ["/bin/bash", "/opt/start.sh"]
