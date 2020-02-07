FROM python:3.6

RUN apt update
RUN apt install -y xvfb x11-utils firefox-esr
RUN pip install flake8 coverage selenium pyvirtualdisplay
RUN wget https://github.com/mozilla/geckodriver/releases/download/v0.26.0/geckodriver-v0.26.0-linux64.tar.gz
RUN tar xzf geckodriver-v0.26.0-linux64.tar.gz
RUN mv geckodriver /usr/local/bin/.
