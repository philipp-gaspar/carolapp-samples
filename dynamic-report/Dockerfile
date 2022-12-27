FROM python:3.10.8-slim-buster

RUN mkdir /app
WORKDIR /app
ADD requirements.txt /app/
RUN pip install -r requirements.txt

ADD . /app

EXPOSE 5000

CMD ["gunicorn", "-b 0.0.0.0:5000", "dashapp"]