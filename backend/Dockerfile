FROM python:3.9

WORKDIR /app

COPY requirements.txt .

ENV PYTHONUNBUFFERED=1

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "kittygram_backend.wsgi"]
