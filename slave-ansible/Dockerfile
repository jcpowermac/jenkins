FROM openshift/jenkins-slave-base-centos7

RUN yum install -y epel-release && \
    INSTALL_PKGS="ansible python-tox" && \
    yum install -y --setopt=tsflags=nodocs $INSTALL_PKGS && \
    rpm -V $INSTALL_PKGS && \
    yum clean all -y

RUN chown -R 1001:0 $HOME && \
    chmod -R g+rw $HOME

USER 1001
