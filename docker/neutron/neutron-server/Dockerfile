FROM kollaglue/fedora-rdo-neutron-base:l3_ovs_wip
MAINTAINER Kolla Project (https://launchpad.net/kolla)

#Install required packages
RUN yum install -y openstack-neutron \
        python-neutronclient \
        mariadb \
        ; yum clean all

VOLUME /var/lib/neutron

EXPOSE 9696

ADD ./start.sh /start.sh
ADD ./check.sh /check.sh

CMD ["/start.sh"]
