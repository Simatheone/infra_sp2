FROM python:3.7-slim

RUN mkdir /api_yamdb_app

COPY requirements.txt /api_yamdb_app

RUN pip3 install -r /api_yamdb_app/requirements.txt --no-cache-dir

COPY . /api_yamdb_app

WORKDIR /api_yamdb_app

CMD [ "gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]