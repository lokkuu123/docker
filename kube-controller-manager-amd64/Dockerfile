FROM k8s.gcr.io/kube-controller-manager-amd64:v1.11.0

#需要使用yum需要执行这一步
RUN yum update
RUN yum install wget -y
RUN wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
RUN yum repolist
RUN rpm -ivh http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm

RUN yum install -y ceph ceph-common
