FROM python:3.9-slim

WORKDIR /app

RUN pip install gunicorn==20.1.0

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

RUN apt-get update && apt-get install -y make

COPY . .

CMD ["make", "run_gunicorn"]
