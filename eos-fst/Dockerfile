FROM owncloud/eos-base:4.6.5

RUN rpm --rebuilddb && yum -y install \
    jq \
    cryptsetup \
    e2fsprogs \
    xfsprogs \
    smartmontools && \
    yum clean all && \
    rm -rf /var/cache/yum

COPY etc/xrd.cf.fst /etc/xrd.cf.fst 
COPY setup /setup
COPY entrypoint /entrypoint
