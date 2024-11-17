FROM ubuntu:latest

WORKDIR /app

COPY . /app

RUN apt-get update -qq && \
    apt-get install -y python3 python3-venv && \
    python3 -m venv venv && \
    source venv/bin/activate && \
    pip install --no-cache-dir -r requirements.txt

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
