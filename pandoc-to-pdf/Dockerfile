FROM ubuntu:18.04

ENV TZ=Europe/London

RUN apt update
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt install -y ruby-full python-pip wget fontconfig libfreetype6 libjpeg-turbo8 libxcb1 \
                   libpng16-16 libx11-6 libxext6 libxrender1 xfonts-base xfonts-75dpi
RUN pip install python-gitlab flake8
RUN gem install mdl
RUN wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.bionic_amd64.deb \
 && dpkg -i wkhtmltox_0.12.5-1.bionic_amd64.deb \
 && rm wkhtmltox_0.12.5-1.bionic_amd64.deb
RUN wget https://github.com/jgm/pandoc/releases/download/2.7.3/pandoc-2.7.3-linux.tar.gz \
 && tar xzf pandoc-2.7.3-linux.tar.gz \
 && mv pandoc-2.7.3/bin/* /usr/local/bin/. \
 && rm pandoc-2.7.3-linux.tar.gz
