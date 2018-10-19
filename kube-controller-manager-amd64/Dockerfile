FROM k8s.gcr.io/kube-controller-manager-amd64:v1.11.0

RUN curl https://raw.githubusercontent.com/ceph/ceph/master/keys/release.asc | apt-key add - && \
    echo deb http://download.ceph.com/debian-hammer/ jessie main | tee /etc/apt/sources.list.d/ceph.list && \
    apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -q -y ceph-common && \
    apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
