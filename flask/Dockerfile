FROM python:3.10.9

WORKDIR /app

ADD . /app

# ENV FLASK_APP=server.py
# ENV FLASK_RUN_HOST=0.0.0.0

COPY requirements.txt ./

RUN pip install --upgrade pip
RUN pip install --upgrade setuptools
RUN pip install -r requirements.txt

# COPY . .
CMD ["uwsgi", "app.ini"]