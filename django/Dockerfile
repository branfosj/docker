FROM python:3.6

RUN apt update

# Django tests
RUN apt install -y xvfb x11-utils firefox-esr
RUN pip install flake8 coverage selenium pyvirtualdisplay
RUN wget https://github.com/mozilla/geckodriver/releases/download/v0.26.0/geckodriver-v0.26.0-linux64.tar.gz \
 && tar xzf geckodriver-v0.26.0-linux64.tar.gz \
 && mv geckodriver /usr/local/bin/.

# pa11y
RUN apt install -y npm libx11-xcb1 libxcomposite1 libxcursor1 libxdamage1 libxi6 libxtst6 libnss3 libcups2 \
  libxrandr2 libasound2 libatk1.0-0 libatk-bridge2.0-0 libgtk-3-0
RUN npm install -g --unsafe-perm=true --allow-root pa11y-ci

# postgres
RUN apt install -y postgresql postgresql-contrib librrd-dev libldap2-dev libsasl2-dev
RUN sed -i 's/peer/trust/g' /etc/postgresql/11/main/pg_hba.conf
RUN service postgresql start
