FROM python:3.7-slim-buster

ENV PYTHONUNBUFFERED 1

WORKDIR /code

COPY requirements.txt /code/

RUN apt update && apt-get install -y gcc graphviz-dev && pip install -r requirements.txt && apt autoremove -y gcc graphviz-dev && apt autoclean -y

COPY . /code/

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]