FROM ubuntu:18.04

#RUN yum install -y epel-release
#RUN yum install -y python2-pip git wget
#RUN yum install -y centos-release-scl-rh centos-release-scl
#RUN sed -i 's/main/main universe multiverse/g' /etc/apt/sources.list
RUN apt update
RUN apt install -y gem python-pip
RUN pip install python-gitlab flake8
#RUN wget https://downloads.wkhtmltopdf.org/0.12/0.12.5/wkhtmltox-0.12.5-1.centos7.x86_64.rpm
RUN wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.bionic_amd64.deb
RUN wget https://github.com/jgm/pandoc/releases/download/2.7.3/pandoc-2.7.3-linux.tar.gz
#RUN yum install -y wkhtmltox-0.12.5-1.centos7.x86_64.rpm
RUN dpkg -i wkhtmltox_0.12.5-1.bionic_amd64.deb
RUN tar xzf pandoc-2.7.3-linux.tar.gz
RUN mv pandoc-2.7.3/bin/* /usr/local/bin/.
RUN gem install mdl
#RUN yum install -y rh-ruby26
#RUN /bin/bash -l -c "source /opt/rh/rh-ruby26/enable && scl enable rh-ruby26 bash && gem install mdl"