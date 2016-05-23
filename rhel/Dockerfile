FROM rhel7

MAINTAINER Kenneth D. Evensen <kevensen@redhat.com>

ENV HOME=/opt/app-root/

RUN yum clean all && \
    yum install -y --setopt=tsflags=nodocs \
                   --disablerepo='*' \
                   --enablerepo='rhel-7-server-rpms' \
                   openssh-clients && \
    yum clean all && \ 
    rm -rf /var/cache/yum/* && \
    mkdir /opt/app-root && \
    mkdir /opt/app-root/.ssh && \
    chmod 0700 /opt/app-root/.ssh && \
    useradd -u 1001 -r -g 0 -d ${HOME} -c "Default Application User" default && \
    chown -R 1001:0 /opt/app-root

ENTRYPOINT while true; do sleep 60; done
