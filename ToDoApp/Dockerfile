FROM python:3.11

WORKDIR /app

COPY requirements.txt /app/

RUN apt-get update && apt-get install libpq-dev -y
RUN pip3 install -r requirements.txt

COPY . /app/

EXPOSE 8000

CMD ["python3.11", "manage.py", "runserver", "0.0.0.0:8000"]
