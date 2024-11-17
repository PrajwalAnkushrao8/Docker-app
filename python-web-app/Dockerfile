FROM amazonlinux:latest

WORKDIR /app

COPY . /app

RUN yum update -y && \
    yum install -y python3 python3-devel git && \
    python3 -m venv venv && \
    source venv/bin/activate && \
    pip install --no-cache-dir -r requirements.txt

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
