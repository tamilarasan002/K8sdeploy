FROM python:3.9-alpine

WORKDIR /app

COPY requirements.txt .
COPY locustfile.py .

RUN pip install --no-cache-dir -r requirements.txt

CMD [ "locust", "-f", "locustfile.py" ]