FROM centos:7

RUN yum -y install epel-release
RUN yum install -y environment-modules python2-pip git
RUN pip install --upgrade pip
RUN pip install --upgrade setuptools==41.6.0
RUN pip install vsc-install~=0.14.13 vsc-base~=2.9.6 python-graph-core python-graph-dot pep8
