FROM python:3.10-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY src/ ./src/

CMD ["gunicorn", "-w", "2", "-b", "0.0.0.0:5000", "src.wsgi:app"]
