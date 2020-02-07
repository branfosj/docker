FROM ubuntu:18.04

RUN apt update
RUN apt install -y gem python-pip
RUN pip install python-gitlab flake8
RUN gem install mdl
RUN wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.bionic_amd64.deb \
 && dpkg -i wkhtmltox_0.12.5-1.bionic_amd64.deb
RUN wget https://github.com/jgm/pandoc/releases/download/2.7.3/pandoc-2.7.3-linux.tar.gz \
 && tar xzf pandoc-2.7.3-linux.tar.gz \
 && mv pandoc-2.7.3/bin/* /usr/local/bin/.
