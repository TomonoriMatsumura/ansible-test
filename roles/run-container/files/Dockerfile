FROM centos:latest

RUN set -x && \
    rm -f /etc/rpm/macros.image-language-conf && \
    sed -i '/^override_install_langs=/d' /etc/yum.conf && \
    yum -y reinstall glibc-common && \
    yum clean all && \
    yum update -y && \
    yum install -y epel-release && \
    yum install -y git && \
    yum install -y expect && \
    yum install -y openssl-devel && \
    yum install -y python-devel && \
    yum install -y python-pip && \
    pip install --upgrade pip && \
    pip install --upgrade setuptools && \
    pip install git+git://github.com/ansible/ansible.git@devel

ENV LANG="ja_JP.UTF-8" \
    LANGUAGE="ja_JP:ja" \
    LC_ALL="ja_JP.UTF-8"
