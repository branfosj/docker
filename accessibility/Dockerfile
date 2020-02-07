FROM python:3.6

RUN apt update
RUN apt install -y npm libx11-xcb1 libxcomposite1 libxcursor1 libxdamage1 libxi6 libxtst6 libnss3 libcups2 libxrandr2 libasound2 libatk1.0-0 libatk-bridge2.0-0 libgtk-3-0
RUN npm install -g --unsafe-perm=true --allow-root pa11y-ci
