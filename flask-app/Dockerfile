FROM python:3.10

COPY requirements.txt /

RUN pip install --upgrade pip
RUN pip install -r /requirements.txt

COPY . /app
WORKDIR /app

EXPOSE 8000

CMD ["gunicorn","--config", "gunicorn_config.py", "app:app"]

