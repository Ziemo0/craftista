FROM python:slim-bookworm

WORKDIR /app

COPY requirements.txt /app/

RUN pip install -r requirements.txt

COPY . /app

EXPOSE 5000

CMD ["gunicorn", "app:app" ,"--bind", "0.0.0.0:5000"]
